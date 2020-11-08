---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzDeviceSecurityGroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzDeviceSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzDeviceSecurityGroup.md
ms.openlocfilehash: 269d333c9b74ed0e3e959ef609531bcea41b724c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94276727"
---
# <span data-ttu-id="dc0fd-101">Set-AzDeviceSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="dc0fd-101">Set-AzDeviceSecurityGroup</span></span>

## <span data-ttu-id="dc0fd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dc0fd-102">SYNOPSIS</span></span>
<span data-ttu-id="dc0fd-103">Cihaz güvenlik grubunu oluştur veya güncelleştir</span><span class="sxs-lookup"><span data-stu-id="dc0fd-103">Create or update device security group</span></span>

## <span data-ttu-id="dc0fd-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="dc0fd-104">SYNTAX</span></span>

### <span data-ttu-id="dc0fd-105">Resourceıdlevelresource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="dc0fd-105">ResourceIdLevelResource (Default)</span></span>
```
Set-AzDeviceSecurityGroup -Name <String> -HubResourceId <String>
 [-ThresholdRule <PSThresholdCustomAlertRule[]>] [-TimeWindowRule <PSTimeWindowCustomAlertRule[]>]
 [-AllowlistRule <PSAllowlistCustomAlertRule[]>] [-DenylistRule <PSDenylistCustomAlertRule[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dc0fd-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="dc0fd-106">InputObject</span></span>
```
Set-AzDeviceSecurityGroup [-ThresholdRule <PSThresholdCustomAlertRule[]>]
 [-TimeWindowRule <PSTimeWindowCustomAlertRule[]>] [-AllowlistRule <PSAllowlistCustomAlertRule[]>]
 [-DenylistRule <PSDenylistCustomAlertRule[]>] -InputObject <PSDeviceSecurityGroup>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dc0fd-107">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="dc0fd-107">ResourceId</span></span>
```
Set-AzDeviceSecurityGroup [-ThresholdRule <PSThresholdCustomAlertRule[]>]
 [-TimeWindowRule <PSTimeWindowCustomAlertRule[]>] [-AllowlistRule <PSAllowlistCustomAlertRule[]>]
 [-DenylistRule <PSDenylistCustomAlertRule[]>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dc0fd-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="dc0fd-108">DESCRIPTION</span></span>
<span data-ttu-id="dc0fd-109">Set-AzDeviceSecurityGroup cmdlet, IoT güvenlik çözümünde tanımlanmış bir cihaz güvenlik grubu oluşturur veya güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="dc0fd-109">The Set-AzDeviceSecurityGroup cmdlet creates or updates a device security group defined in iot security solution.</span></span>

## <span data-ttu-id="dc0fd-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="dc0fd-110">EXAMPLES</span></span>

### <span data-ttu-id="dc0fd-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="dc0fd-111">Example 1</span></span>
```powershell
PS C:\> $TimeWindowSize = New-TimeSpan -Minutes 5
PS C:\> $TimeWindowRule = New-AzDeviceSecurityGroupTimeWindowRuleObject -Type "ActiveConnectionsNotInAllowedRange" -Enabled $true 
-MaxThreshold 30 -MinThreshold 0 -TimeWindowSize $TimeWindowSize
PS C:\> Set-AzDeviceSecurityGroup -Name "MySecurityGroup" 
-HubResourceId "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub" 
-TimeWindowRule $TimeWindowRules

Id: "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub/providers/Microsoft.Security/deviceSecurityGroups/MySecurityGroup"
Name: "MySecurityGroup"
Type: "Microsoft.Security/deviceSecurityGroups"
ThresholdRules: []
TimeWindowRules: [
            {
              RuleType: "ActiveConnectionsNotInAllowedRange"
              DisplayName: "Number of active connections is not in allowed range"
              Description: "Get an alert when the number of active connections of a device in the time window is not in the allowed range"
              IsEnabled: true
              MinThreshold: 0
              MaxThreshold: 0
              TimeWindowSize: "PT5M"
            }]
AllowlistRules: [
            {
              RuleType": "ConnectionToIpNotAllowed",
              DisplayName: "Outbound connection to an ip that isn't allowed"
              Description: "Get an alert when an outbound connection is created between your device and an ip that isn't allowed"
              IsEnabled: false
              ValueType: "IpCidr"
              AllowlistValues: []
            },
            {
              RuleType: "LocalUserNotAllowed"
              DisplayName: "Login by a local user that isn't allowed"
              Description: "Get an alert when a local user that isn't allowed logins to the device"
              IsEnabled: false
              ValueType: "String"
              AllowlistValues: []
            }]
DenylistRules: []
```

<span data-ttu-id="dc0fd-112">"ActiveConnectionsNotInAllowedRange" kural türüyle "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub" IoT Hub 'ından mevcut cihaz güvenlik grubunu güncelleyin</span><span class="sxs-lookup"><span data-stu-id="dc0fd-112">Update existing device security group from IoT Hub "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub" with rule type "ActiveConnectionsNotInAllowedRange"</span></span>

## <span data-ttu-id="dc0fd-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="dc0fd-113">PARAMETERS</span></span>

### <span data-ttu-id="dc0fd-114">-AllowlistRule</span><span class="sxs-lookup"><span data-stu-id="dc0fd-114">-AllowlistRule</span></span>
<span data-ttu-id="dc0fd-115">Liste kurallarına izin ver.</span><span class="sxs-lookup"><span data-stu-id="dc0fd-115">Allow list rules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSAllowlistCustomAlertRule[]
Parameter Sets: ResourceIdLevelResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSAllowlistCustomAlertRule[]
Parameter Sets: InputObject, ResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc0fd-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc0fd-116">-DefaultProfile</span></span>
<span data-ttu-id="dc0fd-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="dc0fd-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc0fd-118">-DenylistRule</span><span class="sxs-lookup"><span data-stu-id="dc0fd-118">-DenylistRule</span></span>
<span data-ttu-id="dc0fd-119">İzin verme listesi kuralları.</span><span class="sxs-lookup"><span data-stu-id="dc0fd-119">Deny list rules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDenylistCustomAlertRule[]
Parameter Sets: ResourceIdLevelResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDenylistCustomAlertRule[]
Parameter Sets: InputObject, ResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc0fd-120">-Hubresourceıd</span><span class="sxs-lookup"><span data-stu-id="dc0fd-120">-HubResourceId</span></span>
<span data-ttu-id="dc0fd-121">IoT Hub kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="dc0fd-121">IoT Hub resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc0fd-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dc0fd-122">-InputObject</span></span>
<span data-ttu-id="dc0fd-123">Giriş nesnesi.</span><span class="sxs-lookup"><span data-stu-id="dc0fd-123">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDeviceSecurityGroup
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dc0fd-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="dc0fd-124">-Name</span></span>
<span data-ttu-id="dc0fd-125">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="dc0fd-125">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc0fd-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="dc0fd-126">-ResourceId</span></span>
<span data-ttu-id="dc0fd-127">Komutu çağırmak istediğiniz güvenlik kaynağının KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="dc0fd-127">ID of the security resource that you want to invoke the command on.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc0fd-128">-ThresholdRule</span><span class="sxs-lookup"><span data-stu-id="dc0fd-128">-ThresholdRule</span></span>
<span data-ttu-id="dc0fd-129">Eşik kuralları.</span><span class="sxs-lookup"><span data-stu-id="dc0fd-129">Threshold rules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSThresholdCustomAlertRule[]
Parameter Sets: ResourceIdLevelResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSThresholdCustomAlertRule[]
Parameter Sets: InputObject, ResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc0fd-130">-TimeWindowRule</span><span class="sxs-lookup"><span data-stu-id="dc0fd-130">-TimeWindowRule</span></span>
<span data-ttu-id="dc0fd-131">Zaman penceresi kuralları.</span><span class="sxs-lookup"><span data-stu-id="dc0fd-131">Time window rules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSTimeWindowCustomAlertRule[]
Parameter Sets: ResourceIdLevelResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSTimeWindowCustomAlertRule[]
Parameter Sets: InputObject, ResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc0fd-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="dc0fd-132">-Confirm</span></span>
<span data-ttu-id="dc0fd-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="dc0fd-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc0fd-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dc0fd-134">-WhatIf</span></span>
<span data-ttu-id="dc0fd-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="dc0fd-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dc0fd-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="dc0fd-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc0fd-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc0fd-137">CommonParameters</span></span>
<span data-ttu-id="dc0fd-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="dc0fd-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc0fd-139">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="dc0fd-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc0fd-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="dc0fd-140">INPUTS</span></span>

### <span data-ttu-id="dc0fd-141">Microsoft. Azure. Commands. Security. model. DeviceSecurityGroups. PSThresholdCustomAlertRule []</span><span class="sxs-lookup"><span data-stu-id="dc0fd-141">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSThresholdCustomAlertRule[]</span></span>

### <span data-ttu-id="dc0fd-142">Microsoft. Azure. Commands. Security. model. DeviceSecurityGroups. PSTimeWindowCustomAlertRule []</span><span class="sxs-lookup"><span data-stu-id="dc0fd-142">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSTimeWindowCustomAlertRule[]</span></span>

### <span data-ttu-id="dc0fd-143">Microsoft. Azure. Commands. Security. model. DeviceSecurityGroups. PSAllowlistCustomAlertRule []</span><span class="sxs-lookup"><span data-stu-id="dc0fd-143">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSAllowlistCustomAlertRule[]</span></span>

### <span data-ttu-id="dc0fd-144">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDenylistCustomAlertRule []</span><span class="sxs-lookup"><span data-stu-id="dc0fd-144">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDenylistCustomAlertRule[]</span></span>

### <span data-ttu-id="dc0fd-145">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDeviceSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="dc0fd-145">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDeviceSecurityGroup</span></span>

### <span data-ttu-id="dc0fd-146">System. String</span><span class="sxs-lookup"><span data-stu-id="dc0fd-146">System.String</span></span>

## <span data-ttu-id="dc0fd-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="dc0fd-147">OUTPUTS</span></span>

### <span data-ttu-id="dc0fd-148">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDeviceSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="dc0fd-148">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDeviceSecurityGroup</span></span>

## <span data-ttu-id="dc0fd-149">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="dc0fd-149">NOTES</span></span>

## <span data-ttu-id="dc0fd-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="dc0fd-150">RELATED LINKS</span></span>
