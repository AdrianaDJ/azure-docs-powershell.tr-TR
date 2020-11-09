---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzDeviceSecurityGroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzDeviceSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzDeviceSecurityGroup.md
ms.openlocfilehash: 3d43407c9f7e58d7a5d29ef56412f6d38c5c957b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94322768"
---
# <span data-ttu-id="8ea0c-101">Get-AzDeviceSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="8ea0c-101">Get-AzDeviceSecurityGroup</span></span>

## <span data-ttu-id="8ea0c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8ea0c-102">SYNOPSIS</span></span>
<span data-ttu-id="8ea0c-103">Cihaz güvenliği alma (IoT Hub güvenliği)</span><span class="sxs-lookup"><span data-stu-id="8ea0c-103">Get device security group (IoT Hub security)</span></span>

## <span data-ttu-id="8ea0c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8ea0c-104">SYNTAX</span></span>

### <span data-ttu-id="8ea0c-105">Resourceıdscope (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="8ea0c-105">ResourceIdScope (Default)</span></span>
```
Get-AzDeviceSecurityGroup -HubResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8ea0c-106">Resourceıdlevelresource</span><span class="sxs-lookup"><span data-stu-id="8ea0c-106">ResourceIdLevelResource</span></span>
```
Get-AzDeviceSecurityGroup -HubResourceId <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8ea0c-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="8ea0c-107">DESCRIPTION</span></span>
<span data-ttu-id="8ea0c-108">Get-AzDeviceSecurityGroup cmdlet, IoT güvenlik çözümünde tanımlanmış bir cihaz güvenlik grubu döndürüyor</span><span class="sxs-lookup"><span data-stu-id="8ea0c-108">The Get-AzDeviceSecurityGroup cmdlet returns a device security group defined in iot security solution</span></span>

## <span data-ttu-id="8ea0c-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8ea0c-109">EXAMPLES</span></span>

### <span data-ttu-id="8ea0c-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="8ea0c-110">Example 1</span></span>
```powershell
PS C:\> Get-AzDeviceSecurityGroup -HubResourceId "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub" -Name "MySecurityGroup" 

Id: "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub/providers/Microsoft.Security/deviceSecurityGroups/MySecurityGroup"
Name: "MySecurityGroup"
Type: "Microsoft.Security/deviceSecurityGroups"
ThresholdRules: []
TimeWindowRules: [
            {
              RuleType: "ActiveConnectionsNotInAllowedRange"
              DisplayName: "Number of active connections is not in allowed range"
              Description: "Get an alert when the number of active connections of a device in the time window is not in the allowed range"
              IsEnabled: false
              MinThreshold: 0
              MaxThreshold: 0
              TimeWindowSize: "PT15M"
            }
            {
              RuleType: "AmqpC2DMessagesNotInAllowedRange"
              DisplayName: "Number of cloud to device messages (AMQP protocol) is not in allowed range"
              Description: "Get an alert when the number of cloud to device messages (AMQP protocol) in the time window is not in the allowed range"
              IsEnabled: false
              MinThreshold: 0
              MaxThreshold: 0
              TimeWindowSize: "PT15M"
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

<span data-ttu-id="8ea0c-111">IoT Hub 'daki "Mysecuritgroup" cihaz güvenlik grubunu reasource ID "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub" ile alma</span><span class="sxs-lookup"><span data-stu-id="8ea0c-111">Get device security group "MySecurityGroup" in IoT Hub with reasource Id "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub"</span></span>

### <span data-ttu-id="8ea0c-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="8ea0c-112">Example 2</span></span>
```powershell
PS C:\> Get-AzDeviceSecurityGroup -HubResourceId "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub" 

Array of security group items like the item returned in example 1
```

<span data-ttu-id="8ea0c-113">IoT Hub 'da aygıt güvenlik grubunun listesini reasource ID "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub" ile alma</span><span class="sxs-lookup"><span data-stu-id="8ea0c-113">Get list of device security group in IoT Hub with reasource Id "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub"</span></span>

## <span data-ttu-id="8ea0c-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8ea0c-114">PARAMETERS</span></span>

### <span data-ttu-id="8ea0c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ea0c-115">-DefaultProfile</span></span>
<span data-ttu-id="8ea0c-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8ea0c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8ea0c-117">-Hubresourceıd</span><span class="sxs-lookup"><span data-stu-id="8ea0c-117">-HubResourceId</span></span>
<span data-ttu-id="8ea0c-118">Komutu çağırmak istediğiniz güvenlik kaynağının KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="8ea0c-118">ID of the security resource that you want to invoke the command on.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ea0c-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="8ea0c-119">-Name</span></span>
<span data-ttu-id="8ea0c-120">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="8ea0c-120">Resource name.</span></span>

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

### <span data-ttu-id="8ea0c-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ea0c-121">CommonParameters</span></span>
<span data-ttu-id="8ea0c-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8ea0c-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ea0c-123">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="8ea0c-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ea0c-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8ea0c-124">INPUTS</span></span>

### <span data-ttu-id="8ea0c-125">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="8ea0c-125">None</span></span>

## <span data-ttu-id="8ea0c-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8ea0c-126">OUTPUTS</span></span>

### <span data-ttu-id="8ea0c-127">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDeviceSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="8ea0c-127">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDeviceSecurityGroup</span></span>

## <span data-ttu-id="8ea0c-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8ea0c-128">NOTES</span></span>

## <span data-ttu-id="8ea0c-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8ea0c-129">RELATED LINKS</span></span>
