---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 7C15B0AA-D97E-4715-9AD4-971731527D09
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/get-azurermsiterecoveryvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryVault.md
ms.openlocfilehash: f3988d28633ba879ebf78c57e235f4f07d6deced
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763972"
---
# <span data-ttu-id="f8d4c-101">Get-AzureRmSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="f8d4c-101">Get-AzureRmSiteRecoveryVault</span></span>

## <span data-ttu-id="f8d4c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f8d4c-102">SYNOPSIS</span></span>
<span data-ttu-id="f8d4c-103">Geçerli aboneliğin site kurtarma şaşırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="f8d4c-103">Gets Site Recovery vaults from the current subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f8d4c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f8d4c-104">SYNTAX</span></span>

```
Get-AzureRmSiteRecoveryVault [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f8d4c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f8d4c-105">DESCRIPTION</span></span>
<span data-ttu-id="f8d4c-106">**Get-AzureRmSiteRecoveryVault** cmdlet 'i, geçerli abonelikteki Azure Site Recovery Kasası veya belirli bir site kurtarma Kasası listesini alır.</span><span class="sxs-lookup"><span data-stu-id="f8d4c-106">The **Get-AzureRmSiteRecoveryVault** cmdlet gets a list of Azure Site Recovery vaults or a specific Site Recovery vault from the current subscription.</span></span>

## <span data-ttu-id="f8d4c-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f8d4c-107">EXAMPLES</span></span>

## <span data-ttu-id="f8d4c-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f8d4c-108">PARAMETERS</span></span>

### <span data-ttu-id="f8d4c-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8d4c-109">-DefaultProfile</span></span>
<span data-ttu-id="f8d4c-110">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f8d4c-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8d4c-111">-Ad</span><span class="sxs-lookup"><span data-stu-id="f8d4c-111">-Name</span></span>
<span data-ttu-id="f8d4c-112">Kasanın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f8d4c-112">Specifies the name of the vault.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8d4c-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8d4c-113">-ResourceGroupName</span></span>
<span data-ttu-id="f8d4c-114">Kurtarma Hizmetleri nesnesinin alınacağı Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f8d4c-114">Specifies the name of the Azure resource group from which to get the recovery services object.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8d4c-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8d4c-115">CommonParameters</span></span>
<span data-ttu-id="f8d4c-116">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f8d4c-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8d4c-117">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8d4c-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8d4c-118">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f8d4c-118">INPUTS</span></span>

### <span data-ttu-id="f8d4c-119">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="f8d4c-119">None</span></span>
<span data-ttu-id="f8d4c-120">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="f8d4c-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f8d4c-121">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f8d4c-121">OUTPUTS</span></span>

### <span data-ttu-id="f8d4c-122">System. Koleksiyonlar. Generic. LIST ' 1 [Microsoft. Azure. Commands. SiteRecovery. Asrkasa]</span><span class="sxs-lookup"><span data-stu-id="f8d4c-122">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.SiteRecovery.ASRVault]</span></span>

## <span data-ttu-id="f8d4c-123">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f8d4c-123">NOTES</span></span>

## <span data-ttu-id="f8d4c-124">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f8d4c-124">RELATED LINKS</span></span>

[<span data-ttu-id="f8d4c-125">New-AzureRmSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="f8d4c-125">New-AzureRmSiteRecoveryVault</span></span>](./New-AzureRmSiteRecoveryVault.md)

[<span data-ttu-id="f8d4c-126">Remove-AzureRmSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="f8d4c-126">Remove-AzureRmSiteRecoveryVault</span></span>](./Remove-AzureRmSiteRecoveryVault.md)
