---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/New-AzDeviceSecurityGroupTimeWindowRuleObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupTimeWindowRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupTimeWindowRuleObject.md
ms.openlocfilehash: f653a71ed00cce72a926259b1f1cfeed026c0624
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94276195"
---
# <span data-ttu-id="82fca-101">New-AzDeviceSecurityGroupTimeWindowRuleObject</span><span class="sxs-lookup"><span data-stu-id="82fca-101">New-AzDeviceSecurityGroupTimeWindowRuleObject</span></span>

## <span data-ttu-id="82fca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="82fca-102">SYNOPSIS</span></span>
<span data-ttu-id="82fca-103">Cihaz güvenlik grubu (IoT güvenliği) için yeni zaman penceresi oluştur kuralı</span><span class="sxs-lookup"><span data-stu-id="82fca-103">Create new time window rule for device security group (IoT Security)</span></span>

## <span data-ttu-id="82fca-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="82fca-104">SYNTAX</span></span>

```
New-AzDeviceSecurityGroupTimeWindowRuleObject -TimeWindowSize <TimeSpan> -MinThreshold <Int32>
 -MaxThreshold <Int32> -Enabled <Boolean> -Type <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="82fca-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="82fca-105">DESCRIPTION</span></span>
<span data-ttu-id="82fca-106">New-AzDeviceSecurityGroupTimeWindowRuleObject cmdlet, IoT güvenlik çözümünde cihaz güvenlik grubu için yeni bir zaman penceresi uyarı kuralları listesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="82fca-106">The New-AzDeviceSecurityGroupTimeWindowRuleObject cmdlet creates a new list of time window alert rules for device security group in IoT security solution.</span></span>

## <span data-ttu-id="82fca-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="82fca-107">EXAMPLES</span></span>

### <span data-ttu-id="82fca-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="82fca-108">Example 1</span></span>
```powershell
PS C:\> $TimeWindowSize = New-TimeSpan -Minutes 5
PS C:\> New-AzDeviceSecurityGroupTimeWindowRuleObject -TimeWindowSize $TimeWindowSize -MinThreshold 0 -MaxThreshold 30 -Enabled $true -Type "ActiveConnectionsNotInAllowedRange"

RuleType: "ActiveConnectionsNotInAllowedRange"
DisplayName: "Number of active connections is not in allowed range"
Description: "Get an alert when the number of active connections of a device in the time window is not in the allowed range"
IsEnabled: false
MinThreshold: 0
MaxThreshold: 30
TimeWindowSize: "PT5M"
```

<span data-ttu-id="82fca-109">"ActiveConnectionsNotInAllowedRange" türünden yeni zaman penceresi oluştur kuralı</span><span class="sxs-lookup"><span data-stu-id="82fca-109">Create new time window rule from "ActiveConnectionsNotInAllowedRange" type</span></span>

## <span data-ttu-id="82fca-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="82fca-110">PARAMETERS</span></span>

### <span data-ttu-id="82fca-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82fca-111">-DefaultProfile</span></span>
<span data-ttu-id="82fca-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="82fca-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="82fca-113">Özellikli</span><span class="sxs-lookup"><span data-stu-id="82fca-113">-Enabled</span></span>
<span data-ttu-id="82fca-114">Kural etkindir.</span><span class="sxs-lookup"><span data-stu-id="82fca-114">Is rule enabled.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82fca-115">-MaxThreshold</span><span class="sxs-lookup"><span data-stu-id="82fca-115">-MaxThreshold</span></span>
<span data-ttu-id="82fca-116">Maksimum eşik.</span><span class="sxs-lookup"><span data-stu-id="82fca-116">Maximum threshold.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82fca-117">-MinThreshold</span><span class="sxs-lookup"><span data-stu-id="82fca-117">-MinThreshold</span></span>
<span data-ttu-id="82fca-118">Minimum eşik.</span><span class="sxs-lookup"><span data-stu-id="82fca-118">Minimum threshold.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82fca-119">-TimeWindowSize</span><span class="sxs-lookup"><span data-stu-id="82fca-119">-TimeWindowSize</span></span>
<span data-ttu-id="82fca-120">Zaman penceresi boyutu.</span><span class="sxs-lookup"><span data-stu-id="82fca-120">Time window size.</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82fca-121">-Tür</span><span class="sxs-lookup"><span data-stu-id="82fca-121">-Type</span></span>
<span data-ttu-id="82fca-122">Kural türü.</span><span class="sxs-lookup"><span data-stu-id="82fca-122">Rule type.</span></span>

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

### <span data-ttu-id="82fca-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82fca-123">CommonParameters</span></span>
<span data-ttu-id="82fca-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="82fca-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82fca-125">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="82fca-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82fca-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="82fca-126">INPUTS</span></span>

### <span data-ttu-id="82fca-127">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="82fca-127">None</span></span>

## <span data-ttu-id="82fca-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="82fca-128">OUTPUTS</span></span>

### <span data-ttu-id="82fca-129">Microsoft. Azure. Commands. Security. model. DeviceSecurityGroups. PSTimeWindowCustomAlertRule</span><span class="sxs-lookup"><span data-stu-id="82fca-129">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSTimeWindowCustomAlertRule</span></span>

## <span data-ttu-id="82fca-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="82fca-130">NOTES</span></span>

## <span data-ttu-id="82fca-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="82fca-131">RELATED LINKS</span></span>
