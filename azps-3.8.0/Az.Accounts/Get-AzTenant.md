---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/get-aztenant
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzTenant.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzTenant.md
ms.openlocfilehash: 4a39853cfaabbee6dc6e9e87e7c504db2f8d53ea
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096407"
---
# <span data-ttu-id="38bf0-101">Get-AzTenant</span><span class="sxs-lookup"><span data-stu-id="38bf0-101">Get-AzTenant</span></span>

## <span data-ttu-id="38bf0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="38bf0-102">SYNOPSIS</span></span>
<span data-ttu-id="38bf0-103">Geçerli Kullanıcı için yetkilendirilmiş kiracıları alır.</span><span class="sxs-lookup"><span data-stu-id="38bf0-103">Gets tenants that are authorized for the current user.</span></span>

## <span data-ttu-id="38bf0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="38bf0-104">SYNTAX</span></span>

```
Get-AzTenant [[-TenantId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="38bf0-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="38bf0-105">DESCRIPTION</span></span>
<span data-ttu-id="38bf0-106">Get-AzTenant cmdlet 'i, geçerli kullanıcı için yetkilendirilmiş kiracıları alır.</span><span class="sxs-lookup"><span data-stu-id="38bf0-106">The Get-AzTenant cmdlet gets tenants authorized for the current user.</span></span>

## <span data-ttu-id="38bf0-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="38bf0-107">EXAMPLES</span></span>

### <span data-ttu-id="38bf0-108">Örnek 1: Tüm kiracıları alma</span><span class="sxs-lookup"><span data-stu-id="38bf0-108">Example 1: Getting all tenants</span></span>
```
PS C:\> Connect-AzAccount
PS C:\> Get-AzTenant

Id                                   Directory
--                                   ---------
xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx microsoft.com
yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy microsoft.com
```

<span data-ttu-id="38bf0-109">Bu örnekte, bir Azure hesabının tüm yetkili kiracıları nasıl alabileceğiniz gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="38bf0-109">This example shows how to get all of the authorized tenants of an Azure account.</span></span>

### <span data-ttu-id="38bf0-110">Örnek 2: belirli bir kiracı alma</span><span class="sxs-lookup"><span data-stu-id="38bf0-110">Example 2: Getting a specific tenant</span></span>
```
PS C:\> Connect-AzAccount
PS C:\> Get-AzTenant -TenantId xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx

Id                                   Directory
--                                   ---------
xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx microsoft.com
```

<span data-ttu-id="38bf0-111">Bu örnekte, bir Azure hesabında belirli bir yetkili kiracının nasıl alınacağı gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="38bf0-111">This example shows how to get a specific authorized tenant of an Azure account.</span></span>

## <span data-ttu-id="38bf0-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="38bf0-112">PARAMETERS</span></span>

### <span data-ttu-id="38bf0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38bf0-113">-DefaultProfile</span></span>
<span data-ttu-id="38bf0-114">Azure ile iletişimde kullanılan kimlik bilgileri, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="38bf0-114">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="38bf0-115">-Tenantıd</span><span class="sxs-lookup"><span data-stu-id="38bf0-115">-TenantId</span></span>
<span data-ttu-id="38bf0-116">Bu cmdlet 'in aldığı kiracının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="38bf0-116">Specifies the ID of the tenant that this cmdlet gets.</span></span>

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

### <span data-ttu-id="38bf0-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38bf0-117">CommonParameters</span></span>
<span data-ttu-id="38bf0-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="38bf0-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38bf0-119">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38bf0-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38bf0-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="38bf0-120">INPUTS</span></span>

### <span data-ttu-id="38bf0-121">System. String</span><span class="sxs-lookup"><span data-stu-id="38bf0-121">System.String</span></span>

## <span data-ttu-id="38bf0-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="38bf0-122">OUTPUTS</span></span>

### <span data-ttu-id="38bf0-123">Microsoft. Azure. Commands. Profile. modeller. PSAzureTenant</span><span class="sxs-lookup"><span data-stu-id="38bf0-123">Microsoft.Azure.Commands.Profile.Models.PSAzureTenant</span></span>

## <span data-ttu-id="38bf0-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="38bf0-124">NOTES</span></span>

## <span data-ttu-id="38bf0-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="38bf0-125">RELATED LINKS</span></span>