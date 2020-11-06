---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 556A9F12-DF72-468F-9C3F-A747CC70BD2F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/test-azurermdnsavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Test-AzureRmDnsAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Test-AzureRmDnsAvailability.md
ms.openlocfilehash: 348fd7e97566520b27163de91d4d52162d4c3978
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591334"
---
# <span data-ttu-id="ad67a-101">Test-AzureRmDnsAvailability</span><span class="sxs-lookup"><span data-stu-id="ad67a-101">Test-AzureRmDnsAvailability</span></span>

## <span data-ttu-id="ad67a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ad67a-102">SYNOPSIS</span></span>
<span data-ttu-id="ad67a-103">Cloudapp.azure.com bölgesindeki bir etki alanı adının kullanıma uygun olup olmadığını denetler.</span><span class="sxs-lookup"><span data-stu-id="ad67a-103">Checks whether a domain name in the cloudapp.azure.com zone is available for use.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ad67a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ad67a-104">SYNTAX</span></span>

```
Test-AzureRmDnsAvailability -DomainNameLabel <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ad67a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ad67a-105">DESCRIPTION</span></span>
<span data-ttu-id="ad67a-106">Cloudapp.azure.com bölgesindeki bir etki alanı adının kullanıma uygun olup olmadığını denetler.</span><span class="sxs-lookup"><span data-stu-id="ad67a-106">Checks whether a domain name in the cloudapp.azure.com zone is available for use.</span></span>

## <span data-ttu-id="ad67a-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ad67a-107">EXAMPLES</span></span>

### <span data-ttu-id="ad67a-108">Örnek 1: contoso.cloudapp.azure.com 'in kullanılabilir olup olmadığını denetleyin.</span><span class="sxs-lookup"><span data-stu-id="ad67a-108">Example 1: Check if contoso.cloudapp.azure.com is available for use.</span></span>
```
Test-AzureRmDnsAvailability -DomainNameLabel contoso -Location westus
```

## <span data-ttu-id="ad67a-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ad67a-109">PARAMETERS</span></span>

### <span data-ttu-id="ad67a-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad67a-110">-DefaultProfile</span></span>
<span data-ttu-id="ad67a-111">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ad67a-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ad67a-112">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="ad67a-112">-DomainNameLabel</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DomainQualifiedName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad67a-113">-Konum</span><span class="sxs-lookup"><span data-stu-id="ad67a-113">-Location</span></span>
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

### <span data-ttu-id="ad67a-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad67a-114">CommonParameters</span></span>
<span data-ttu-id="ad67a-115">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ad67a-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad67a-116">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad67a-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad67a-117">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ad67a-117">INPUTS</span></span>

### <span data-ttu-id="ad67a-118">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="ad67a-118">None</span></span>

## <span data-ttu-id="ad67a-119">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ad67a-119">OUTPUTS</span></span>

### <span data-ttu-id="ad67a-120">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ad67a-120">System.Boolean</span></span>

## <span data-ttu-id="ad67a-121">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ad67a-121">NOTES</span></span>

## <span data-ttu-id="ad67a-122">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ad67a-122">RELATED LINKS</span></span>
