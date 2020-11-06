---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: D19488C1-9E87-4F1A-94E3-8AFDE6AFC982
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryStorageClassificationMapping.md
ms.openlocfilehash: 1c8d061dae3d2334b422e6f9e4e3c2b7bb75abcc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593787"
---
# <span data-ttu-id="aae17-101">Get-AzureRmSiteRecoveryStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="aae17-101">Get-AzureRmSiteRecoveryStorageClassificationMapping</span></span>

## <span data-ttu-id="aae17-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aae17-102">SYNOPSIS</span></span>
<span data-ttu-id="aae17-103">Site kurtarmada bir depolama sınıflandırması eşlemesi alır.</span><span class="sxs-lookup"><span data-stu-id="aae17-103">Gets a storage classification mapping in Site Recovery.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aae17-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="aae17-104">SYNTAX</span></span>

### <span data-ttu-id="aae17-105">Varsayılan (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="aae17-105">Default (Default)</span></span>
```
Get-AzureRmSiteRecoveryStorageClassificationMapping [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="aae17-106">ByName</span><span class="sxs-lookup"><span data-stu-id="aae17-106">ByName</span></span>
```
Get-AzureRmSiteRecoveryStorageClassificationMapping -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="aae17-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="aae17-107">DESCRIPTION</span></span>
<span data-ttu-id="aae17-108">**Get-AzureRmSiteRecoveryStorageClassificationMapping** cmdlet 'ı Azure Site Recovery 'de bir depolama sınıflandırması eşlemesi alır.</span><span class="sxs-lookup"><span data-stu-id="aae17-108">The **Get-AzureRmSiteRecoveryStorageClassificationMapping** cmdlet gets a storage classification mapping in Azure Site Recovery.</span></span>

## <span data-ttu-id="aae17-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="aae17-109">EXAMPLES</span></span>

## <span data-ttu-id="aae17-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="aae17-110">PARAMETERS</span></span>

### <span data-ttu-id="aae17-111">-Ad</span><span class="sxs-lookup"><span data-stu-id="aae17-111">-Name</span></span>
<span data-ttu-id="aae17-112">Bu cmdlet 'in aldığı depolama sınıflandırması eşlemesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="aae17-112">Specifies the name of the storage classification mapping that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aae17-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aae17-113">-DefaultProfile</span></span>
<span data-ttu-id="aae17-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="aae17-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aae17-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aae17-115">CommonParameters</span></span>
<span data-ttu-id="aae17-116">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="aae17-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aae17-117">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aae17-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aae17-118">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="aae17-118">INPUTS</span></span>

## <span data-ttu-id="aae17-119">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="aae17-119">OUTPUTS</span></span>

### <span data-ttu-id="aae17-120">System. Koleksiyonlar. Generic. IEnumerable ' 1 [Microsoft. Azure. Commands. SiteRecovery. Asrstorageclassıficationmapping]</span><span class="sxs-lookup"><span data-stu-id="aae17-120">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRStorageClassificationMapping]</span></span>

## <span data-ttu-id="aae17-121">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="aae17-121">NOTES</span></span>

## <span data-ttu-id="aae17-122">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="aae17-122">RELATED LINKS</span></span>

[<span data-ttu-id="aae17-123">New-AzureRmSiteRecoveryStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="aae17-123">New-AzureRmSiteRecoveryStorageClassificationMapping</span></span>](./New-AzureRmSiteRecoveryStorageClassificationMapping.md)

[<span data-ttu-id="aae17-124">Remove-AzureRmSiteRecoveryStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="aae17-124">Remove-AzureRmSiteRecoveryStorageClassificationMapping</span></span>](./Remove-AzureRmSiteRecoveryStorageClassificationMapping.md)
