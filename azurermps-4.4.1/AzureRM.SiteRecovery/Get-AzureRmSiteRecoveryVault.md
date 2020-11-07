---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 7C15B0AA-D97E-4715-9AD4-971731527D09
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryVault.md
ms.openlocfilehash: 37e0096dd6f279c13909f1b542e603faebfd1e97
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763616"
---
# <span data-ttu-id="2c9c8-101">Get-AzureRmSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="2c9c8-101">Get-AzureRmSiteRecoveryVault</span></span>

## <span data-ttu-id="2c9c8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2c9c8-102">SYNOPSIS</span></span>
<span data-ttu-id="2c9c8-103">Geçerli aboneliğin site kurtarma şaşırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="2c9c8-103">Gets Site Recovery vaults from the current subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2c9c8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2c9c8-104">SYNTAX</span></span>

```
Get-AzureRmSiteRecoveryVault [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2c9c8-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="2c9c8-105">DESCRIPTION</span></span>
<span data-ttu-id="2c9c8-106">**Get-AzureRmSiteRecoveryVault** cmdlet 'i, geçerli abonelikteki Azure Site Recovery Kasası veya belirli bir site kurtarma Kasası listesini alır.</span><span class="sxs-lookup"><span data-stu-id="2c9c8-106">The **Get-AzureRmSiteRecoveryVault** cmdlet gets a list of Azure Site Recovery vaults or a specific Site Recovery vault from the current subscription.</span></span>

## <span data-ttu-id="2c9c8-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2c9c8-107">EXAMPLES</span></span>

## <span data-ttu-id="2c9c8-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2c9c8-108">PARAMETERS</span></span>

### <span data-ttu-id="2c9c8-109">-Ad</span><span class="sxs-lookup"><span data-stu-id="2c9c8-109">-Name</span></span>
<span data-ttu-id="2c9c8-110">Kasanın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2c9c8-110">Specifies the name of the vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c9c8-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c9c8-111">-ResourceGroupName</span></span>
<span data-ttu-id="2c9c8-112">Kurtarma Hizmetleri nesnesinin alınacağı Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2c9c8-112">Specifies the name of the Azure resource group from which to get the recovery services object.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c9c8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c9c8-113">-DefaultProfile</span></span>
<span data-ttu-id="2c9c8-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2c9c8-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2c9c8-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c9c8-115">CommonParameters</span></span>
<span data-ttu-id="2c9c8-116">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2c9c8-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c9c8-117">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c9c8-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c9c8-118">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2c9c8-118">INPUTS</span></span>

## <span data-ttu-id="2c9c8-119">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2c9c8-119">OUTPUTS</span></span>

### <span data-ttu-id="2c9c8-120">System. Koleksiyonlar. Generic. LIST ' 1 [Microsoft. Azure. Commands. SiteRecovery. Asrkasa]</span><span class="sxs-lookup"><span data-stu-id="2c9c8-120">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.SiteRecovery.ASRVault]</span></span>

## <span data-ttu-id="2c9c8-121">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2c9c8-121">NOTES</span></span>

## <span data-ttu-id="2c9c8-122">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2c9c8-122">RELATED LINKS</span></span>

[<span data-ttu-id="2c9c8-123">New-AzureRmSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="2c9c8-123">New-AzureRmSiteRecoveryVault</span></span>](./New-AzureRmSiteRecoveryVault.md)

[<span data-ttu-id="2c9c8-124">Remove-AzureRmSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="2c9c8-124">Remove-AzureRmSiteRecoveryVault</span></span>](./Remove-AzureRmSiteRecoveryVault.md)
