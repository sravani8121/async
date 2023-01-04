console.log('person1: shows ticket');
console.log('person2: shows ticket');

const preMovie = async () =>{
    const promiseWifeBringingTics = new Promise((resolve,reject) =>{
        setTimeout(() =>resolve('ticket'), 3000);
    });
    const getPopcorn = new Promise((resolve,reject) =>resolve(`popcorn`));
    const addButter = new Promise((resolve,reject) =>resolve(`butter`));

    let ticket = await promiseWifeBringingTics;
    console.log(`wife:i have the ${ticket}`);
    console.log('husband:we should go in');
    console.log('wife: no iam hungry');

    let popcorn = await getPopcorn;
    console.log(`husband:i got some ${popcorn}`);
    console.log('husband:we have to go in');
    console.log('wife:i need butter on my popcorn');

    let butter = await addButter;
    console.log(`husband: i got some ${butter} on popcorn`);
    console.log(`husband:anything else`);
    console.log(`wife:lets go we are getting late`);
    console.log(`husband:thank you for reminder`);

    return ticket;
}
preMovie().then((m) => console.log(`person3: shows${m}`));

console.log('person4:shows ticket');
console.log('person5:shows ticket');
