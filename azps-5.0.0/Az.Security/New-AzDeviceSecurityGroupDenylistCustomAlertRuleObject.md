---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject.md
ms.openlocfilehash: 0e1de96eed8b3f1174bebd6a127db91f9733dd67
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94276734"
---
# <span data-ttu-id="beb2f-101">New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject</span><span class="sxs-lookup"><span data-stu-id="beb2f-101">New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject</span></span>

## <span data-ttu-id="beb2f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="beb2f-102">SYNOPSIS</span></span>
<span data-ttu-id="beb2f-103">Yeni Reddedilenler Listesi Oluştur cihaz güvenlik grubu (IoT güvenliği) için özel uyarı kuralı</span><span class="sxs-lookup"><span data-stu-id="beb2f-103">Create new deny list custom alert rule for device security group (IoT Security)</span></span>

## <span data-ttu-id="beb2f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="beb2f-104">SYNTAX</span></span>

```
New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject -Enabled <Boolean> -Type <String>
 -DenylistValue <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="beb2f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="beb2f-105">DESCRIPTION</span></span>
<span data-ttu-id="beb2f-106">New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject cmdlet, IoT güvenlik çözümünde cihaz güvenlik grubu için yeni bir özel uyarı kuralları listesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="beb2f-106">The New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject cmdlet creates a new list of denyed custom alert rules for device security group in IoT security solution.</span></span>

## <span data-ttu-id="beb2f-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="beb2f-107">EXAMPLES</span></span>

### <span data-ttu-id="beb2f-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="beb2f-108">Example 1</span></span>
```powershell
PS C:\> New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject -Enabled $false -Type "SomeRuleType" -DenylistValue @()

RuleType: "SomeRuleType"
DisplayName: "Display name for some rule type"
Description: "Description for some rule type"
IsEnabled: false
ValueType: "String"
DenylistValues: []
```

<span data-ttu-id="beb2f-109">Yeni Reddedilenler Listesi Oluştur "Someruletür" ve</span><span class="sxs-lookup"><span data-stu-id="beb2f-109">Create new deny list custom alert rule with rull type "SomeRuleType" and status set to desable</span></span>

## <span data-ttu-id="beb2f-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="beb2f-110">PARAMETERS</span></span>

### <span data-ttu-id="beb2f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="beb2f-111">-DefaultProfile</span></span>
<span data-ttu-id="beb2f-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="beb2f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="beb2f-113">-DenylistValue</span><span class="sxs-lookup"><span data-stu-id="beb2f-113">-DenylistValue</span></span>
<span data-ttu-id="beb2f-114">Liste değerlerini reddedin.</span><span class="sxs-lookup"><span data-stu-id="beb2f-114">Deny list values.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="beb2f-115">Özellikli</span><span class="sxs-lookup"><span data-stu-id="beb2f-115">-Enabled</span></span>
<span data-ttu-id="beb2f-116">Kural etkindir.</span><span class="sxs-lookup"><span data-stu-id="beb2f-116">Is rule enabled.</span></span>

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

### <span data-ttu-id="beb2f-117">-Tür</span><span class="sxs-lookup"><span data-stu-id="beb2f-117">-Type</span></span>
<span data-ttu-id="beb2f-118">Kural türü.</span><span class="sxs-lookup"><span data-stu-id="beb2f-118">Rule type.</span></span>

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

### <span data-ttu-id="beb2f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="beb2f-119">CommonParameters</span></span>
<span data-ttu-id="beb2f-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="beb2f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="beb2f-121">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="beb2f-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="beb2f-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="beb2f-122">INPUTS</span></span>

### <span data-ttu-id="beb2f-123">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="beb2f-123">None</span></span>

## <span data-ttu-id="beb2f-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="beb2f-124">OUTPUTS</span></span>

### <span data-ttu-id="beb2f-125">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDenylistCustomAlertRule</span><span class="sxs-lookup"><span data-stu-id="beb2f-125">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDenylistCustomAlertRule</span></span>

## <span data-ttu-id="beb2f-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="beb2f-126">NOTES</span></span>

## <span data-ttu-id="beb2f-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="beb2f-127">RELATED LINKS</span></span>
