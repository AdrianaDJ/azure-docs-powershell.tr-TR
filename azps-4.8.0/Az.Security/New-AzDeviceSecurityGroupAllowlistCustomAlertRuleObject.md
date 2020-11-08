---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject.md
ms.openlocfilehash: c9f2a8440f2ed91003dc818824a8d7b8662a96a3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94107630"
---
# <span data-ttu-id="3de4d-101">New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject</span><span class="sxs-lookup"><span data-stu-id="3de4d-101">New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject</span></span>

## <span data-ttu-id="3de4d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3de4d-102">SYNOPSIS</span></span>
<span data-ttu-id="3de4d-103">Yeni izin verilenler listesi oluştur cihaz güvenlik grubu (IoT güvenliği) için özel uyarı kuralı</span><span class="sxs-lookup"><span data-stu-id="3de4d-103">Create new allow list custom alert rule for device security group (IoT Security)</span></span>

## <span data-ttu-id="3de4d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3de4d-104">SYNTAX</span></span>

```
New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject -Enabled <Boolean> -Type <String>
 -AllowlistValue <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3de4d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="3de4d-105">DESCRIPTION</span></span>
<span data-ttu-id="3de4d-106">New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject cmdlet, IoT güvenlik çözümünde cihaz güvenlik grubu için izin verilen özel uyarı kurallarının yeni bir listesini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="3de4d-106">The New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject cmdlet creates a new list of allowed custom alert rules for device security group in IoT security solution.</span></span>

## <span data-ttu-id="3de4d-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3de4d-107">EXAMPLES</span></span>

### <span data-ttu-id="3de4d-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="3de4d-108">Example 1</span></span>
```powershell
PS C:\> New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject -Enabled $false -Type "LocalUserNotAllowed" -AllowlistValue @()

RuleType: "LocalUserNotAllowed"
DisplayName: "Login by a local user that isn't allowed"
Description: "Get an alert when a local user that isn't allowed logins to the device"
IsEnabled: false
ValueType: "String"
AllowlistValues: []
```

<span data-ttu-id="3de4d-109">"LocalUserNotAllowed" türünden "LocalUserNotAllowed" türünden devre dışı</span><span class="sxs-lookup"><span data-stu-id="3de4d-109">Create new allow list custom alert rull from type "LocalUserNotAllowed" with status set to disable</span></span>

## <span data-ttu-id="3de4d-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3de4d-110">PARAMETERS</span></span>

### <span data-ttu-id="3de4d-111">-AllowlistValue</span><span class="sxs-lookup"><span data-stu-id="3de4d-111">-AllowlistValue</span></span>
<span data-ttu-id="3de4d-112">Liste değerlerine izin ver.</span><span class="sxs-lookup"><span data-stu-id="3de4d-112">Allow list values.</span></span>

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

### <span data-ttu-id="3de4d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3de4d-113">-DefaultProfile</span></span>
<span data-ttu-id="3de4d-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3de4d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3de4d-115">Özellikli</span><span class="sxs-lookup"><span data-stu-id="3de4d-115">-Enabled</span></span>
<span data-ttu-id="3de4d-116">Kural etkindir.</span><span class="sxs-lookup"><span data-stu-id="3de4d-116">Is rule enabled.</span></span>

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

### <span data-ttu-id="3de4d-117">-Tür</span><span class="sxs-lookup"><span data-stu-id="3de4d-117">-Type</span></span>
<span data-ttu-id="3de4d-118">Kural türü.</span><span class="sxs-lookup"><span data-stu-id="3de4d-118">Rule type.</span></span>

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

### <span data-ttu-id="3de4d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3de4d-119">CommonParameters</span></span>
<span data-ttu-id="3de4d-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3de4d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3de4d-121">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="3de4d-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3de4d-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3de4d-122">INPUTS</span></span>

### <span data-ttu-id="3de4d-123">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="3de4d-123">None</span></span>

## <span data-ttu-id="3de4d-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3de4d-124">OUTPUTS</span></span>

### <span data-ttu-id="3de4d-125">Microsoft. Azure. Commands. Security. model. DeviceSecurityGroups. PSAllowlistCustomAlertRule</span><span class="sxs-lookup"><span data-stu-id="3de4d-125">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSAllowlistCustomAlertRule</span></span>

## <span data-ttu-id="3de4d-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3de4d-126">NOTES</span></span>

## <span data-ttu-id="3de4d-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3de4d-127">RELATED LINKS</span></span>
