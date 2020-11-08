---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeeringserviceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringServiceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringServiceProvider.md
ms.openlocfilehash: 8341f465bab88f8d8a60e5f171f883dbb9a2467e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94277574"
---
# <span data-ttu-id="0ef4e-101">Get-AzPeeringServiceProvider</span><span class="sxs-lookup"><span data-stu-id="0ef4e-101">Get-AzPeeringServiceProvider</span></span>

## <span data-ttu-id="0ef4e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0ef4e-102">SYNOPSIS</span></span>
<span data-ttu-id="0ef4e-103">Microsoft ile ortaklık hizmet sağlayıcılarının ortaklık listesini alır.</span><span class="sxs-lookup"><span data-stu-id="0ef4e-103">Gets a list of peering service providers partnered with Microsoft.</span></span>

## <span data-ttu-id="0ef4e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0ef4e-104">SYNTAX</span></span>

```
Get-AzPeeringServiceProvider [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0ef4e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="0ef4e-105">DESCRIPTION</span></span>
<span data-ttu-id="0ef4e-106">Liste eşleme hizmeti sağlayıcıları</span><span class="sxs-lookup"><span data-stu-id="0ef4e-106">List peering service providers</span></span>

## <span data-ttu-id="0ef4e-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0ef4e-107">EXAMPLES</span></span>

### <span data-ttu-id="0ef4e-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="0ef4e-108">Example 1</span></span>
```powershell
PS C:\> Get-AzPeeringServiceProvider

ServiceProviderName Name      Id Type
------------------- ----      -- ----
TestPeer1           TestPeer1    Microsoft.Peering/peeringServiceProviders
```

<span data-ttu-id="0ef4e-109">Kullanılabilir eşleme hizmeti sağlayıcılarını alır</span><span class="sxs-lookup"><span data-stu-id="0ef4e-109">Gets available peering service providers</span></span>

## <span data-ttu-id="0ef4e-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0ef4e-110">PARAMETERS</span></span>

### <span data-ttu-id="0ef4e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ef4e-111">-DefaultProfile</span></span>
<span data-ttu-id="0ef4e-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0ef4e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0ef4e-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ef4e-113">CommonParameters</span></span>
<span data-ttu-id="0ef4e-114">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0ef4e-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ef4e-115">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="0ef4e-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ef4e-116">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0ef4e-116">INPUTS</span></span>

### <span data-ttu-id="0ef4e-117">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="0ef4e-117">None</span></span>

## <span data-ttu-id="0ef4e-118">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0ef4e-118">OUTPUTS</span></span>

### <span data-ttu-id="0ef4e-119">Microsoft. Azure. PowerShell. cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0ef4e-119">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServiceProvider</span></span>

## <span data-ttu-id="0ef4e-120">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0ef4e-120">NOTES</span></span>

## <span data-ttu-id="0ef4e-121">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0ef4e-121">RELATED LINKS</span></span>
