---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject.md
ms.openlocfilehash: 848882438cfe41a8c736bfcde780aa0421f73a68
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94278013"
---
# <span data-ttu-id="9e109-101">New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject</span><span class="sxs-lookup"><span data-stu-id="9e109-101">New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject</span></span>

## <span data-ttu-id="9e109-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9e109-102">SYNOPSIS</span></span>
<span data-ttu-id="9e109-103">Cihaz güvenlik grubu (IoT güvenliği) için yeni eşik özel uyarı kuralı oluştur</span><span class="sxs-lookup"><span data-stu-id="9e109-103">Create new threshold custom alert rule for device security group (IoT Security)</span></span>

## <span data-ttu-id="9e109-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9e109-104">SYNTAX</span></span>

```
New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject -MinThreshold <Int32> -MaxThreshold <Int32>
 -Enabled <Boolean> -Type <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9e109-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="9e109-105">DESCRIPTION</span></span>
<span data-ttu-id="9e109-106">New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject cmdlet, IoT güvenlik çözümünde cihaz güvenlik grubu için bir eşik özel uyarı kuralları listesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9e109-106">The New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject cmdlet creates a new list of threshold custom alert rules for device security group in IoT security solution.</span></span>

## <span data-ttu-id="9e109-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9e109-107">EXAMPLES</span></span>

### <span data-ttu-id="9e109-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="9e109-108">Example 1</span></span>
```powershell
PS C:\> New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject -MinThreshold 0 -MaxThreshold 10 -Enabled $true -Type "SomeRuleType"

RuleType: "SomeRuleType"
DisplayName: "Display name for some rule type"
Description: "Description for some rule type"
IsEnabled: false
MinThreshold: 0
MaxThreshold: 10
```

<span data-ttu-id="9e109-109">"SomeRuleType" türünden yeni eşik özel uyarı kuralı oluşturma</span><span class="sxs-lookup"><span data-stu-id="9e109-109">Create new threshold custom alert rule from type "SomeRuleType" with status enabled ant values for minimum and maximum threshold</span></span>

## <span data-ttu-id="9e109-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9e109-110">PARAMETERS</span></span>

### <span data-ttu-id="9e109-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e109-111">-DefaultProfile</span></span>
<span data-ttu-id="9e109-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9e109-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9e109-113">Özellikli</span><span class="sxs-lookup"><span data-stu-id="9e109-113">-Enabled</span></span>
<span data-ttu-id="9e109-114">Kural etkindir.</span><span class="sxs-lookup"><span data-stu-id="9e109-114">Is rule enabled.</span></span>

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

### <span data-ttu-id="9e109-115">-MaxThreshold</span><span class="sxs-lookup"><span data-stu-id="9e109-115">-MaxThreshold</span></span>
<span data-ttu-id="9e109-116">Maksimum eşik.</span><span class="sxs-lookup"><span data-stu-id="9e109-116">Maximum threshold.</span></span>

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

### <span data-ttu-id="9e109-117">-MinThreshold</span><span class="sxs-lookup"><span data-stu-id="9e109-117">-MinThreshold</span></span>
<span data-ttu-id="9e109-118">Minimum eşik.</span><span class="sxs-lookup"><span data-stu-id="9e109-118">Minimum threshold.</span></span>

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

### <span data-ttu-id="9e109-119">-Tür</span><span class="sxs-lookup"><span data-stu-id="9e109-119">-Type</span></span>
<span data-ttu-id="9e109-120">Kural türü.</span><span class="sxs-lookup"><span data-stu-id="9e109-120">Rule type.</span></span>

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

### <span data-ttu-id="9e109-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e109-121">CommonParameters</span></span>
<span data-ttu-id="9e109-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9e109-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e109-123">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="9e109-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e109-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9e109-124">INPUTS</span></span>

### <span data-ttu-id="9e109-125">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="9e109-125">None</span></span>

## <span data-ttu-id="9e109-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9e109-126">OUTPUTS</span></span>

### <span data-ttu-id="9e109-127">Microsoft. Azure. Commands. Security. model. DeviceSecurityGroups. PSThresholdCustomAlertRule</span><span class="sxs-lookup"><span data-stu-id="9e109-127">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSThresholdCustomAlertRule</span></span>

## <span data-ttu-id="9e109-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9e109-128">NOTES</span></span>

## <span data-ttu-id="9e109-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9e109-129">RELATED LINKS</span></span>
