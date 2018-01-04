'use strict';

// Basic Variables.
let splitter = "<hr>";
let panelText = "<center><b><u>Control Panel</u></b></center>";
let nl = "<br>";
	
// BUILD
exports.commands = {
	p: 'panel',
	panel : function (target, room, user, connection) {
		// REQUESTED
		if (!user.isStaff) return false;
		// REQUIRED
		let targetUser = this.targetUserOrSelf(target, user.group === ' ');
		if (!targetUser) return this.errorReply("Target must be online.");
		let connectedIp = Object.keys(targetUser.ips);

		// USER INFO
		let userInfo = "<font color='maroon'><b>Alt(s): </b></font>" + targetUser.name + "";
		
		// BUILD
		let ButtonInfoKick = "<button name='send' value='/kick " + targetUser + "'><font color='blue'>Kick User (Room)</button></font>";
		let ButtonInfoKickServer = "<button name='send' value='/kickserver " + targetUser + "'><font color='blue'>Kick User (Serveur)</button></font>";
		let ButtonInfoWarn = "<button name='send' value='/warn " + targetUser + ", (Warn par le panel)'><font color='blue'>Warn User</button></font>";
		let ButtonInfoDayMute = "<button name='send' value='/daymute " + targetUser + ", (Daymute par le panel)'><font color='blue'>Mute User (Jour)</button></font>";
		let ButtonInfoMute = "<button name='send' value='/mute " + targetUser + ", (Muted par le panel)'><font color='blue'>Mute User (7 Mins)</button></font>";
		let ButtonInfoHourMute = "<button name='send' value='/hourmute " + targetUser + ", (Hourmute par le panel)'><font color='red'>Mute User (1 Hr)</button></font>";
		let ButtonInfoDayLock = "<button name='send' value='/daylock " + targetUser + ", (Daylock par le panel)'><font color='red'>Lock User (1 Jour)</button></font>";
		let ButtonInfoLock = "<button name='send' value='/lock " + targetUser + ", (Lock par le panel)'><font color='red'>Lock User (Défaut)</button></font>";
		let ButtonInfoForceLock = "<button name='send' value='/forcelock " + targetUser + ", (Lock par le panel)'><font color='red'>Lock User (Force)</button></font>";
		let ButtonInfoNameLock = "<button name='send' value='/namelock " + targetUser + ", (Namelock par le panel)'><font color='red'>Lock User (Name)</button></font>";
		let ButtonInfoBan = "<button name='send' value='/globalban " + targetUser + ", (Ban par le panel)'><font color='red'>Ban User (Défaut)</button></font>";
		let ButtonInfoForceBan = "<button name='send' value='/forceglobalban " + targetUser + ", (Ban par le panel)'><font color='red'>Ban User (Force)</button></font>";
		
		// MAIN BUILD
		this.sendReplyBox(splitter + panelText + splitter + userInfo + splitter + ButtonInfoKick + ButtonInfoKickServer + ButtonInfoWarn + ButtonInfoDayMute + ButtonInfoMute + nl + ButtonInfoHourMute + ButtonInfoDayLock + ButtonInfoLock + ButtonInfoForceLock + ButtonInfoNameLock + ButtonInfoBan + ButtonInfoForceBan + splitter);
	}
};
