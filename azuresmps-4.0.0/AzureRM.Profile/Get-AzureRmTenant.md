---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2cabb88c490c7fdea56fd5ffde280cfd55bc8f3d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93571745"
---
# <span data-ttu-id="a59b0-101">Get-AzureRmTenant</span><span class="sxs-lookup"><span data-stu-id="a59b0-101">Get-AzureRmTenant</span></span>

## <span data-ttu-id="a59b0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a59b0-102">SYNOPSIS</span></span>
<span data-ttu-id="a59b0-103">Geçerli Kullanıcı için yetkilendirilmiş kiracıları alır.</span><span class="sxs-lookup"><span data-stu-id="a59b0-103">Gets tenants that are authorized for the current user.</span></span>

## <span data-ttu-id="a59b0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a59b0-104">SYNTAX</span></span>

```
Get-AzureRmTenant [[-TenantId] <String>] [<CommonParameters>]
```

## <span data-ttu-id="a59b0-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a59b0-105">DESCRIPTION</span></span>
<span data-ttu-id="a59b0-106">Get-AzureRmTenant cmdlet 'i, geçerli kullanıcı için yetkilendirilmiş kiracıları alır.</span><span class="sxs-lookup"><span data-stu-id="a59b0-106">The Get-AzureRmTenant cmdlet gets tenants authorized for the current user.</span></span>

## <span data-ttu-id="a59b0-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a59b0-107">EXAMPLES</span></span>

### <span data-ttu-id="a59b0-108">Örnek 1: Tüm kiracıları alma</span><span class="sxs-lookup"><span data-stu-id="a59b0-108">Example 1: Getting all tenants</span></span>
```
PS C:\> Add-AzureRmAccount
PS C:\> Get-AzureRmTenant

TenantId : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Domain   : microsoft.com

TenantId : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Domain   : microsoft.com
```

<span data-ttu-id="a59b0-109">Bu örnekte, bir Azure hesabının tüm yetkili kiracıları nasıl alabileceğiniz gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="a59b0-109">This example shows how to get all of the authorized tenants of an Azure account.</span></span>

### <span data-ttu-id="a59b0-110">Örnek 2: belirli bir kiracı alma</span><span class="sxs-lookup"><span data-stu-id="a59b0-110">Example 2: Getting a specific tenant</span></span>
```
PS C:\> Add-AzureRmAccount
PS C:\> Get-AzureRmTenant -TenantId xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx

TenantId : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Domain   : microsoft.com
```

<span data-ttu-id="a59b0-111">Bu örnekte, bir Azure hesabında belirli bir yetkili kiracının nasıl alınacağı gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="a59b0-111">This example shows how to get a specific authorized tenant of an Azure account.</span></span>

## <span data-ttu-id="a59b0-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a59b0-112">PARAMETERS</span></span>

### <span data-ttu-id="a59b0-113">-Tenantıd</span><span class="sxs-lookup"><span data-stu-id="a59b0-113">-TenantId</span></span>
<span data-ttu-id="a59b0-114">Bu cmdlet 'in aldığı kiracının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="a59b0-114">Specifies the ID of the tenant that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Domain, Tenant

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a59b0-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a59b0-115">CommonParameters</span></span>
<span data-ttu-id="a59b0-116">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a59b0-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a59b0-117">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a59b0-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a59b0-118">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a59b0-118">INPUTS</span></span>

## <span data-ttu-id="a59b0-119">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a59b0-119">OUTPUTS</span></span>

### <span data-ttu-id="a59b0-120">PSAzureTenant</span><span class="sxs-lookup"><span data-stu-id="a59b0-120">PSAzureTenant</span></span>
<span data-ttu-id="a59b0-121">Bu cmdlet, geçerli hesap için yetkilendirilmiş kiracıları için kiracı KIMLIĞI ve ilişkili etki alanı bilgilerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="a59b0-121">This cmdlet returns the tenant ID and associated domain information for tenants authorized for the current account.</span></span>

## <span data-ttu-id="a59b0-122">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a59b0-122">NOTES</span></span>

## <span data-ttu-id="a59b0-123">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a59b0-123">RELATED LINKS</span></span>

