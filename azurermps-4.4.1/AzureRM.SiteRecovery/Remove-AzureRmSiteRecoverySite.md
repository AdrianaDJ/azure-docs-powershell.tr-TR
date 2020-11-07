---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: DE1D5A0D-2545-4F01-98B5-684ED0D25230
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoverySite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoverySite.md
ms.openlocfilehash: f052b11a11fa77047d424b7045b127a75043cc25
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763316"
---
# <span data-ttu-id="e2ab0-101">Remove-AzureRmSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="e2ab0-101">Remove-AzureRmSiteRecoverySite</span></span>

## <span data-ttu-id="e2ab0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e2ab0-102">SYNOPSIS</span></span>
<span data-ttu-id="e2ab0-103">Geçerli kasadan site kurtarma sitesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="e2ab0-103">Removes a Site Recovery site from the current vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e2ab0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e2ab0-104">SYNTAX</span></span>

```
Remove-AzureRmSiteRecoverySite -Site <ASRSite> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e2ab0-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e2ab0-105">DESCRIPTION</span></span>
<span data-ttu-id="e2ab0-106">**Remove-AzureRmSiteRecoverySite** cmdlet 'i geçerli kasadan bir Azure Site Recovery sitesini siler.</span><span class="sxs-lookup"><span data-stu-id="e2ab0-106">The **Remove-AzureRmSiteRecoverySite** cmdlet deletes an Azure Site Recovery site from the current vault.</span></span>

## <span data-ttu-id="e2ab0-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e2ab0-107">EXAMPLES</span></span>

## <span data-ttu-id="e2ab0-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e2ab0-108">PARAMETERS</span></span>

### <span data-ttu-id="e2ab0-109">-Force</span><span class="sxs-lookup"><span data-stu-id="e2ab0-109">-Force</span></span>
<span data-ttu-id="e2ab0-110">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="e2ab0-110">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2ab0-111">-Site</span><span class="sxs-lookup"><span data-stu-id="e2ab0-111">-Site</span></span>
<span data-ttu-id="e2ab0-112">Site kurtarma site nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e2ab0-112">Specifies the Site Recovery site object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRSite
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e2ab0-113">-Onay</span><span class="sxs-lookup"><span data-stu-id="e2ab0-113">-Confirm</span></span>
<span data-ttu-id="e2ab0-114">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e2ab0-114">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2ab0-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2ab0-115">-WhatIf</span></span>
<span data-ttu-id="e2ab0-116">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e2ab0-116">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="e2ab0-117">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e2ab0-117">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2ab0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2ab0-118">-DefaultProfile</span></span>
<span data-ttu-id="e2ab0-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e2ab0-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2ab0-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2ab0-120">CommonParameters</span></span>
<span data-ttu-id="e2ab0-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e2ab0-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2ab0-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2ab0-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2ab0-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e2ab0-123">INPUTS</span></span>

### <span data-ttu-id="e2ab0-124">ASRSite</span><span class="sxs-lookup"><span data-stu-id="e2ab0-124">ASRSite</span></span>
<span data-ttu-id="e2ab0-125">' Site ' parametresi ardışık düzen</span><span class="sxs-lookup"><span data-stu-id="e2ab0-125">Parameter 'Site' accepts value of type 'ASRSite' from the pipeline</span></span>

## <span data-ttu-id="e2ab0-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e2ab0-126">OUTPUTS</span></span>

## <span data-ttu-id="e2ab0-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e2ab0-127">NOTES</span></span>

## <span data-ttu-id="e2ab0-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e2ab0-128">RELATED LINKS</span></span>

[<span data-ttu-id="e2ab0-129">Get-AzureRmSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="e2ab0-129">Get-AzureRmSiteRecoverySite</span></span>](./Get-AzureRmSiteRecoverySite.md)

[<span data-ttu-id="e2ab0-130">New-AzureRmSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="e2ab0-130">New-AzureRmSiteRecoverySite</span></span>](./New-AzureRmSiteRecoverySite.md)
