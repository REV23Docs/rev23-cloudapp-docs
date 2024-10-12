# Services

A **Service** represents a a project, which contains a collection of _related_ procedures performed on a customer by a service provider. _Related_ is the key word.

- one tattoo that was started and finished in one day.
- a tattoo that requires multiple days to complete.
- one or more piercings in the same sitting.
- a microblading session and the follow-up weeks later.

As such, a service is locked to one provider and one customer. Meaning, every session in the service must be done by the same person.

A **Session** represents what procedure was done, and the details of that procedure. A service can contain one or more sessions.

> If you're coming from REV23 Desktop, the idea of services is slightly different. In Desktop, a Service was represented as a service as a single session. There was no separation between the two objects.

When a customer uses [Kiosk](kiosk.md) to fill out a release form, a service is created containing a session for each service type they selected. Here's some common scenarios to better your understanding.

- If they selected Tattoo, a service is created with one (1) tattoo session.
- If they selected Piercing, a service is created with one session for each piercing type select. If they selected Lobe and Tragus, two (2) sessions are created in the same service.

The benefit of sessions is they allow you to track a longer running service. For example multi-day tattoo sessions that span over the course of a few months. You can add a new session to the existing service to track the progress of that single piece of work. Likewise, Microbladers may wish to contain a touch-up session inside the same service, easily referring back to to photos and pigment formulas. For piercers, a service generally will only reflect the piercings done in that sitting.

### Completing a Service
When you are done with a service it can be completed, though this step is not necessary. Completing a service prevents any further sessions from being added to it, and will automatically end any sessions, thus generating the release form.

<a href="#sessions"></a>
## Sessions

Sessions are really the single most important piece of the REV23 puzzle.

A session represents details about the work such as placement, description, price, as well as the forms that were filled out. Release forms are per **session**, meaning each piercing you do in a service for example has its own session, which has its own release form; each addition you add to a tattoo back piece has it's own release form, etc...

Sessions can include as much, or as little information as you would like to add, as long as it conforms with your local health department.

You can track supplies such as needles, ink, disposable grips, tubes and detailed jewelry information. All of this info can be added to the release form as required.

<a href="#release-forms"></a>
### Release Forms
We've established that release forms are filled out in [Kiosk](kiosk.md) sessions. But where do they go? How do you see them?

When a session is **Ended**, any forms that were filled out are then generated. It is not until this happens that the release form is finalized. This gives you the opportunity to get all supplies added (which are required to be on the release form by more and more health departments).

Release Forms are sent to a processing queue in the REV23 cloud and generated as a PDF and stored securely. You can view the progress of their generation and the final document in the **Forms** section of the session.

### Adding Sessions

You can add a new session to a service using the Add Session action. On iPad you will be prompted with two options. Signed or Unsigned.

An **Unsigned** session will create the session but not have the customer fill out a form. If you do not require paperwork for touch-ups, jewelry downsizing, change outs, etc.. you can add this as a session to the existing service.

A **Signed** session will being a Kiosk flow for the customer to answer quetions and sign, thereby creating a form that will be generated with the session is ended. In this Kiosk flow, some steps are skipped since the app already knows who the client is, though they are allowed to update info if needed. If you require paperwork for touch-ups, or want to add another piercing after the service has already been created, you should choose this option.


# Webhooks

Services support the following [webhook](./webhooks.md) events:

|Event|Permission|Description|
|-|-|-|
|**service.created**|read:service| A service object was created. |
|**servicesession.created**|read:service| A session object was created. |
|**releaseform.generated**|read:service| A release form PDF was generated. |