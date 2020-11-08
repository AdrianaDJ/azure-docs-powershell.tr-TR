---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 556A9F12-DF72-468F-9C3F-A747CC70BD2F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/test-azdnsavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzDnsAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzDnsAvailability.md
ms.openlocfilehash: 2ee468c47f22e90ce47b003dcae1becfb905134e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94265862"
---
# <span data-ttu-id="3dbc3-101">Test-AzDnsAvailability</span><span class="sxs-lookup"><span data-stu-id="3dbc3-101">Test-AzDnsAvailability</span></span>

## <span data-ttu-id="3dbc3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3dbc3-102">SYNOPSIS</span></span>
<span data-ttu-id="3dbc3-103">Cloudapp.azure.com bölgesindeki bir etki alanı adının kullanıma uygun olup olmadığını denetler.</span><span class="sxs-lookup"><span data-stu-id="3dbc3-103">Checks whether a domain name in the cloudapp.azure.com zone is available for use.</span></span>

## <span data-ttu-id="3dbc3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3dbc3-104">SYNTAX</span></span>

```
Test-AzDnsAvailability -DomainNameLabel <String> -Location <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3dbc3-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="3dbc3-105">DESCRIPTION</span></span>
<span data-ttu-id="3dbc3-106">Cloudapp.azure.com bölgesindeki bir etki alanı adının kullanıma uygun olup olmadığını denetler.</span><span class="sxs-lookup"><span data-stu-id="3dbc3-106">Checks whether a domain name in the cloudapp.azure.com zone is available for use.</span></span>

## <span data-ttu-id="3dbc3-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3dbc3-107">EXAMPLES</span></span>

### <span data-ttu-id="3dbc3-108">Örnek 1: contoso.westus.cloudapp.azure.com 'in kullanılabilir olup olmadığını denetleyin.</span><span class="sxs-lookup"><span data-stu-id="3dbc3-108">Example 1: Check if contoso.westus.cloudapp.azure.com is available for use.</span></span>
```
Test-AzDnsAvailability -DomainNameLabel contoso -Location westus
```

## <span data-ttu-id="3dbc3-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3dbc3-109">PARAMETERS</span></span>

### <span data-ttu-id="3dbc3-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3dbc3-110">-DefaultProfile</span></span>
<span data-ttu-id="3dbc3-111">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3dbc3-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3dbc3-112">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="3dbc3-112">-DomainNameLabel</span></span>
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

### <span data-ttu-id="3dbc3-113">-Konum</span><span class="sxs-lookup"><span data-stu-id="3dbc3-113">-Location</span></span>
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

### <span data-ttu-id="3dbc3-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3dbc3-114">CommonParameters</span></span>
<span data-ttu-id="3dbc3-115">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3dbc3-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3dbc3-116">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3dbc3-116">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3dbc3-117">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3dbc3-117">INPUTS</span></span>

### <span data-ttu-id="3dbc3-118">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="3dbc3-118">None</span></span>

## <span data-ttu-id="3dbc3-119">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3dbc3-119">OUTPUTS</span></span>

### <span data-ttu-id="3dbc3-120">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3dbc3-120">System.Boolean</span></span>

## <span data-ttu-id="3dbc3-121">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3dbc3-121">NOTES</span></span>

## <span data-ttu-id="3dbc3-122">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3dbc3-122">RELATED LINKS</span></span>
