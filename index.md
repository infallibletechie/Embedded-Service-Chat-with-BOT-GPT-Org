<html>
<style type='text/css'>
	.embeddedServiceHelpButton .helpButton .uiButton {
		background-color: #005290;
		font-family: "Arial", sans-serif;
	}
	.embeddedServiceHelpButton .helpButton .uiButton:focus {
		outline: 1px solid #005290;
	}
</style>

<script type='text/javascript' src='https://service.force.com/embeddedservice/5.0/esw.min.js'></script>
<script type='text/javascript'>
	var initESW = function(gslbBaseURL) {
		embedded_svc.settings.displayHelpButton = true; //Or false
		embedded_svc.settings.language = ''; //For example, enter 'en' or 'en-US'

		embedded_svc.settings.enabledFeatures = ['LiveAgent'];
		embedded_svc.settings.entryFeature = 'LiveAgent';
		embedded_svc.settings.prepopulatedPrechatFields = {
		    FirstName: "Test",
		    LastName: "Test",
		    Email: "test@test.com",
		    Subject: "Testing"
		};

		embedded_svc.init(
			'https://infallibletechiegpt.my.salesforce.com',
			'https://infallibletechiegpt.my.site.com/consumer',
			gslbBaseURL,
			'00DHn000002Tnsw',
			'Embedded_Service_Chat_with_BOT',
			{
				baseLiveAgentContentURL: 'https://c.la3-c1-ia6.salesforceliveagent.com/content',
				deploymentId: '572Hn0000011K2z',
				buttonId: '573Hn0000011K35',
				baseLiveAgentURL: 'https://d.la3-c1-ia6.salesforceliveagent.com/chat',
				eswLiveAgentDevName: 'EmbeddedServiceLiveAgent_Parent04IHn0000010xbjMAA_18c9773eb9b',
				isOfflineSupportEnabled: false
			}
		);
	};

	if (!window.embedded_svc) {
		var s = document.createElement('script');
		s.setAttribute('src', 'https://infallibletechiegpt.my.salesforce.com/embeddedservice/5.0/esw.min.js');
		s.onload = function() {
			initESW(null);
		};
		document.body.appendChild(s);
	} else {
		initESW('https://service.force.com');
	}
</script>
</html>
