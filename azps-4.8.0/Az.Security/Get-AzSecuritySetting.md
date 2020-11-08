---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecuritySetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySetting.md
ms.openlocfilehash: 708fb6b3807e874d00c3e555ef84973572edcd1c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94266382"
---
# <span data-ttu-id="baea4-101">Get-AzSecuritySetting</span><span class="sxs-lookup"><span data-stu-id="baea4-101">Get-AzSecuritySetting</span></span>

## <span data-ttu-id="baea4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="baea4-102">SYNOPSIS</span></span>
<span data-ttu-id="baea4-103">Azure Güvenlik Merkezi 'nde güvenlik ayarlarını alma</span><span class="sxs-lookup"><span data-stu-id="baea4-103">Get security settings in Azure Security Center</span></span>

## <span data-ttu-id="baea4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="baea4-104">SYNTAX</span></span>

### <span data-ttu-id="baea4-105">SubscriptionScope (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="baea4-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecuritySetting [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="baea4-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="baea4-106">SubscriptionLevelResource</span></span>
```
Get-AzSecuritySetting -SettingName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="baea4-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="baea4-107">DESCRIPTION</span></span>
<span data-ttu-id="baea4-108">Get-AzSecuritySetting cmdlet 'i Azure Güvenlik Merkezi 'nde güvenlik ayarlarını alma.</span><span class="sxs-lookup"><span data-stu-id="baea4-108">The Get-AzSecuritySetting cmdlet get security settings in Azure Security Center.</span></span>

## <span data-ttu-id="baea4-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="baea4-109">EXAMPLES</span></span>

### <span data-ttu-id="baea4-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="baea4-110">Example 1</span></span>
```powershell
PS C:\> Set-AzSecuritySetting -SettingName "MCAS"

Id: "/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/settings/MCAS"
Name: "MCAS"
Type: "Microsoft.Security/settings"
Enabled: true
```

<span data-ttu-id="baea4-111">Bir MCAS veri dışarı aktarma ayarı alır</span><span class="sxs-lookup"><span data-stu-id="baea4-111">Gets an MCAS data export setting</span></span>   

## <span data-ttu-id="baea4-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="baea4-112">PARAMETERS</span></span>

### <span data-ttu-id="baea4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="baea4-113">-DefaultProfile</span></span>
<span data-ttu-id="baea4-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="baea4-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="baea4-115">-SettingName</span><span class="sxs-lookup"><span data-stu-id="baea4-115">-SettingName</span></span>
<span data-ttu-id="baea4-116">Ayar adı.</span><span class="sxs-lookup"><span data-stu-id="baea4-116">Setting name.</span></span> <span data-ttu-id="baea4-117">(MCAS/WDATP)</span><span class="sxs-lookup"><span data-stu-id="baea4-117">(MCAS/WDATP)</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="baea4-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="baea4-118">CommonParameters</span></span>
<span data-ttu-id="baea4-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="baea4-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="baea4-120">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="baea4-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="baea4-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="baea4-121">INPUTS</span></span>

### <span data-ttu-id="baea4-122">System. String</span><span class="sxs-lookup"><span data-stu-id="baea4-122">System.String</span></span>

## <span data-ttu-id="baea4-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="baea4-123">OUTPUTS</span></span>

### <span data-ttu-id="baea4-124">Microsoft. Azure. Commands. Security. model. Settings. PSSecuritySetting</span><span class="sxs-lookup"><span data-stu-id="baea4-124">Microsoft.Azure.Commands.Security.Models.Settings.PSSecuritySetting</span></span>
### <span data-ttu-id="baea4-125">Microsoft. Azure. Commands. Security. model. Settings. PSSecurityDataExportSetting</span><span class="sxs-lookup"><span data-stu-id="baea4-125">Microsoft.Azure.Commands.Security.Models.Settings.PSSecurityDataExportSetting</span></span>

## <span data-ttu-id="baea4-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="baea4-126">NOTES</span></span>

## <span data-ttu-id="baea4-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="baea4-127">RELATED LINKS</span></span>
