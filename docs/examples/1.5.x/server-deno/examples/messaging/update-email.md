import { Client, Messaging } from "https://deno.land/x/appwrite/mod.ts";

const client = new Client()
    .setEndpoint('https://cloud.appwrite.io/v1') // Your API Endpoint
    .setProject('5df5acd0d48c2') // Your project ID
    .setKey('919c2d18fb5d4...a2ae413da83346ad2'); // Your secret API key

const messaging = new Messaging(client);

const response = await messaging.updateEmail(
    '<MESSAGE_ID>', // messageId
    [], // topics (optional)
    [], // users (optional)
    [], // targets (optional)
    '<SUBJECT>', // subject (optional)
    '<CONTENT>', // content (optional)
    false, // draft (optional)
    false, // html (optional)
    [], // cc (optional)
    [], // bcc (optional)
    '', // scheduledAt (optional)
    [] // attachments (optional)
);
