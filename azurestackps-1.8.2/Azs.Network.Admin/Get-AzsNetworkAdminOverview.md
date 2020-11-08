---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3f5fbef7c67676f16793b63a8448517ca24aa7e5
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94106615"
---
# <span data-ttu-id="6ec35-101">Get-AzsNetworkAdminOverview</span><span class="sxs-lookup"><span data-stu-id="6ec35-101">Get-AzsNetworkAdminOverview</span></span>

## <span data-ttu-id="6ec35-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6ec35-102">SYNOPSIS</span></span>
<span data-ttu-id="6ec35-103">Ağ kaynağı sağlayıcısının durumuna genel bakış.</span><span class="sxs-lookup"><span data-stu-id="6ec35-103">Get an overview of the state of the network resource provider.</span></span>

## <span data-ttu-id="6ec35-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6ec35-104">SYNTAX</span></span>

```
Get-AzsNetworkAdminOverview [<CommonParameters>]
```

## <span data-ttu-id="6ec35-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="6ec35-105">DESCRIPTION</span></span>
<span data-ttu-id="6ec35-106">Ağ kaynağı sağlayıcısının durumuna genel bakış.</span><span class="sxs-lookup"><span data-stu-id="6ec35-106">Get an overview of the state of the network resource provider.</span></span> <span data-ttu-id="6ec35-107">Tek tek özellikler, bileşene göre ayrıntılı kaynak kullanımı ve sistem durumu sağlar.</span><span class="sxs-lookup"><span data-stu-id="6ec35-107">Individual properties provide detailed counts of resource usage and health by component.</span></span>

## <span data-ttu-id="6ec35-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6ec35-108">EXAMPLES</span></span>

### <span data-ttu-id="6ec35-109">ÖRNEK 1</span><span class="sxs-lookup"><span data-stu-id="6ec35-109">EXAMPLE 1</span></span>
```
Get-AzsNetworkAdminOverview
```

<span data-ttu-id="6ec35-110">Ağ yöneticisine genel bakış.</span><span class="sxs-lookup"><span data-stu-id="6ec35-110">Get network admin overview.</span></span>

### <span data-ttu-id="6ec35-111">ÖRNEK 2</span><span class="sxs-lookup"><span data-stu-id="6ec35-111">EXAMPLE 2</span></span>
```
(Get-AzsNetworkAdminOverview).PublicIpAddressUsage
```

<span data-ttu-id="6ec35-112">Genel IP adresi kullanımını edinin.</span><span class="sxs-lookup"><span data-stu-id="6ec35-112">Get public ip address usage.</span></span>

## <span data-ttu-id="6ec35-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6ec35-113">PARAMETERS</span></span>

### <span data-ttu-id="6ec35-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ec35-114">CommonParameters</span></span>
<span data-ttu-id="6ec35-115">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6ec35-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ec35-116">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ec35-116">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ec35-117">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6ec35-117">INPUTS</span></span>

## <span data-ttu-id="6ec35-118">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6ec35-118">OUTPUTS</span></span>

### <span data-ttu-id="6ec35-119">Microsoft. AzureStack. Management. Network. admin. model. AdminOverview</span><span class="sxs-lookup"><span data-stu-id="6ec35-119">Microsoft.AzureStack.Management.Network.Admin.Models.AdminOverview</span></span>

## <span data-ttu-id="6ec35-120">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6ec35-120">NOTES</span></span>

## <span data-ttu-id="6ec35-121">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6ec35-121">RELATED LINKS</span></span>
