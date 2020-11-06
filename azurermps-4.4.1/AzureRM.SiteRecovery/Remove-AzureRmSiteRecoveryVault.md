---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 63E9894A-3AC5-4397-9B21-D0A72EBA5C4B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryVault.md
ms.openlocfilehash: e5d85c6cdc30ff00d2a35bba6d1a79119cbaddd2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592544"
---
# <span data-ttu-id="c8f72-101">Remove-AzureRmSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="c8f72-101">Remove-AzureRmSiteRecoveryVault</span></span>

## <span data-ttu-id="c8f72-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c8f72-102">SYNOPSIS</span></span>
<span data-ttu-id="c8f72-103">Site kurtarma kasasından çıkarır.</span><span class="sxs-lookup"><span data-stu-id="c8f72-103">Removes a Site Recovery vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c8f72-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c8f72-104">SYNTAX</span></span>

```
Remove-AzureRmSiteRecoveryVault -Vault <ASRVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c8f72-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c8f72-105">DESCRIPTION</span></span>
<span data-ttu-id="c8f72-106">**Remove-AzureRmSiteRecoveryVault** cmdlet 'ı bir Azure Site kurtarma Kasası siler.</span><span class="sxs-lookup"><span data-stu-id="c8f72-106">The **Remove-AzureRmSiteRecoveryVault** cmdlet deletes an Azure Site Recovery vault.</span></span>

## <span data-ttu-id="c8f72-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c8f72-107">EXAMPLES</span></span>

## <span data-ttu-id="c8f72-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c8f72-108">PARAMETERS</span></span>

### <span data-ttu-id="c8f72-109">-Kasa</span><span class="sxs-lookup"><span data-stu-id="c8f72-109">-Vault</span></span>
<span data-ttu-id="c8f72-110">Site Recovery kasa nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c8f72-110">Specifies the Site Recovery vault object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRVault
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c8f72-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8f72-111">-DefaultProfile</span></span>
<span data-ttu-id="c8f72-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c8f72-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c8f72-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8f72-113">CommonParameters</span></span>
<span data-ttu-id="c8f72-114">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c8f72-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8f72-115">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c8f72-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8f72-116">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c8f72-116">INPUTS</span></span>

### <span data-ttu-id="c8f72-117">Asrkasa</span><span class="sxs-lookup"><span data-stu-id="c8f72-117">ASRVault</span></span>
<span data-ttu-id="c8f72-118">Parametre ' kasa ', ardışık düzenin ' Asrkasa ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="c8f72-118">Parameter 'Vault' accepts value of type 'ASRVault' from the pipeline</span></span>

## <span data-ttu-id="c8f72-119">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c8f72-119">OUTPUTS</span></span>

## <span data-ttu-id="c8f72-120">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c8f72-120">NOTES</span></span>

## <span data-ttu-id="c8f72-121">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c8f72-121">RELATED LINKS</span></span>

[<span data-ttu-id="c8f72-122">Get-AzureRmSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="c8f72-122">Get-AzureRmSiteRecoveryVault</span></span>](./Get-AzureRmSiteRecoveryVault.md)

[<span data-ttu-id="c8f72-123">New-AzureRmSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="c8f72-123">New-AzureRmSiteRecoveryVault</span></span>](./New-AzureRmSiteRecoveryVault.md)
