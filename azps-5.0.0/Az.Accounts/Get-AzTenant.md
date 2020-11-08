---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/get-aztenant
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzTenant.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzTenant.md
ms.openlocfilehash: 936eb5bb7f49c2530a325b3bfa8c369b8f097711
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94276488"
---
# <span data-ttu-id="63030-101">Get-AzTenant</span><span class="sxs-lookup"><span data-stu-id="63030-101">Get-AzTenant</span></span>

## <span data-ttu-id="63030-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="63030-102">SYNOPSIS</span></span>
<span data-ttu-id="63030-103">Geçerli Kullanıcı için yetkilendirilmiş kiracıları alır.</span><span class="sxs-lookup"><span data-stu-id="63030-103">Gets tenants that are authorized for the current user.</span></span>

## <span data-ttu-id="63030-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="63030-104">SYNTAX</span></span>

```
Get-AzTenant [[-TenantId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="63030-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="63030-105">DESCRIPTION</span></span>
<span data-ttu-id="63030-106">Get-AzTenant cmdlet 'i, geçerli kullanıcı için yetkilendirilmiş kiracıları alır.</span><span class="sxs-lookup"><span data-stu-id="63030-106">The Get-AzTenant cmdlet gets tenants authorized for the current user.</span></span>

## <span data-ttu-id="63030-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="63030-107">EXAMPLES</span></span>

### <span data-ttu-id="63030-108">Örnek 1: Tüm kiracıları alma</span><span class="sxs-lookup"><span data-stu-id="63030-108">Example 1: Getting all tenants</span></span>
```
PS C:\> Connect-AzAccount
PS C:\> Get-AzTenant

Id                                   Name        Category Domains
--                                   ----------- -------- -------
xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Microsoft   Home     {test0.com, test1.com, test2.microsoft.com, test3.microsoft.com...}
yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy Testhost    Home     testhost.onmicrosoft.com
```

<span data-ttu-id="63030-109">Bu örnekte, bir Azure hesabının tüm yetkili kiracıları nasıl alabileceğiniz gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="63030-109">This example shows how to get all of the authorized tenants of an Azure account.</span></span>

### <span data-ttu-id="63030-110">Örnek 2: belirli bir kiracı alma</span><span class="sxs-lookup"><span data-stu-id="63030-110">Example 2: Getting a specific tenant</span></span>
```
PS C:\> Connect-AzAccount
PS C:\> Get-AzTenant -TenantId xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx

Id                                   Name        Category Domains
--                                   ----------- -------- -------
xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Microsoft   Home     {test0.com, test1.com, test2.microsoft.com, test3.microsoft.com...}
```

<span data-ttu-id="63030-111">Bu örnekte, bir Azure hesabında belirli bir yetkili kiracının nasıl alınacağı gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="63030-111">This example shows how to get a specific authorized tenant of an Azure account.</span></span>

## <span data-ttu-id="63030-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="63030-112">PARAMETERS</span></span>

### <span data-ttu-id="63030-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63030-113">-DefaultProfile</span></span>
<span data-ttu-id="63030-114">Azure ile iletişimde kullanılan kimlik bilgileri, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="63030-114">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="63030-115">-Tenantıd</span><span class="sxs-lookup"><span data-stu-id="63030-115">-TenantId</span></span>
<span data-ttu-id="63030-116">Bu cmdlet 'in aldığı kiracının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="63030-116">Specifies the ID of the tenant that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Domain, Tenant

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63030-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63030-117">CommonParameters</span></span>
<span data-ttu-id="63030-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="63030-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63030-119">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="63030-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63030-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="63030-120">INPUTS</span></span>

### <span data-ttu-id="63030-121">System. String</span><span class="sxs-lookup"><span data-stu-id="63030-121">System.String</span></span>

## <span data-ttu-id="63030-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="63030-122">OUTPUTS</span></span>

### <span data-ttu-id="63030-123">Microsoft. Azure. Commands. Profile. modeller. PSAzureTenant</span><span class="sxs-lookup"><span data-stu-id="63030-123">Microsoft.Azure.Commands.Profile.Models.PSAzureTenant</span></span>

## <span data-ttu-id="63030-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="63030-124">NOTES</span></span>

## <span data-ttu-id="63030-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="63030-125">RELATED LINKS</span></span>
