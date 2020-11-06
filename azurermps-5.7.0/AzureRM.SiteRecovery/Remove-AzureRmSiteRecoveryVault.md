---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 63E9894A-3AC5-4397-9B21-D0A72EBA5C4B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/remove-azurermsiterecoveryvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryVault.md
ms.openlocfilehash: 70d0876be32b80d314dfb7a464d0626b7c534fea
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573258"
---
# <span data-ttu-id="49971-101">Remove-AzureRmSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="49971-101">Remove-AzureRmSiteRecoveryVault</span></span>

## <span data-ttu-id="49971-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="49971-102">SYNOPSIS</span></span>
<span data-ttu-id="49971-103">Site kurtarma kasasından çıkarır.</span><span class="sxs-lookup"><span data-stu-id="49971-103">Removes a Site Recovery vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="49971-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="49971-104">SYNTAX</span></span>

```
Remove-AzureRmSiteRecoveryVault -Vault <ASRVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="49971-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="49971-105">DESCRIPTION</span></span>
<span data-ttu-id="49971-106">**Remove-AzureRmSiteRecoveryVault** cmdlet 'ı bir Azure Site kurtarma Kasası siler.</span><span class="sxs-lookup"><span data-stu-id="49971-106">The **Remove-AzureRmSiteRecoveryVault** cmdlet deletes an Azure Site Recovery vault.</span></span>

## <span data-ttu-id="49971-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="49971-107">EXAMPLES</span></span>

## <span data-ttu-id="49971-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="49971-108">PARAMETERS</span></span>

### <span data-ttu-id="49971-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49971-109">-DefaultProfile</span></span>
<span data-ttu-id="49971-110">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="49971-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="49971-111">-Kasa</span><span class="sxs-lookup"><span data-stu-id="49971-111">-Vault</span></span>
<span data-ttu-id="49971-112">Site Recovery kasa nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="49971-112">Specifies the Site Recovery vault object.</span></span>

```yaml
Type: ASRVault
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="49971-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49971-113">CommonParameters</span></span>
<span data-ttu-id="49971-114">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="49971-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49971-115">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49971-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49971-116">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="49971-116">INPUTS</span></span>

### <span data-ttu-id="49971-117">Asrkasa</span><span class="sxs-lookup"><span data-stu-id="49971-117">ASRVault</span></span>
<span data-ttu-id="49971-118">Parametre ' kasa ', ardışık düzenin ' Asrkasa ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="49971-118">Parameter 'Vault' accepts value of type 'ASRVault' from the pipeline</span></span>

## <span data-ttu-id="49971-119">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="49971-119">OUTPUTS</span></span>

## <span data-ttu-id="49971-120">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="49971-120">NOTES</span></span>

## <span data-ttu-id="49971-121">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="49971-121">RELATED LINKS</span></span>

[<span data-ttu-id="49971-122">Get-AzureRmSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="49971-122">Get-AzureRmSiteRecoveryVault</span></span>](./Get-AzureRmSiteRecoveryVault.md)

[<span data-ttu-id="49971-123">New-AzureRmSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="49971-123">New-AzureRmSiteRecoveryVault</span></span>](./New-AzureRmSiteRecoveryVault.md)
