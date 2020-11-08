---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storage/new-Azstorageaccountmanagementpolicyfilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountManagementPolicyFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountManagementPolicyFilter.md
ms.openlocfilehash: 48ae8b87671e52abe4d109025048fe1e4aeca117
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098620"
---
# <span data-ttu-id="a1500-101">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="a1500-101">New-AzStorageAccountManagementPolicyFilter</span></span>

## <span data-ttu-id="a1500-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a1500-102">SYNOPSIS</span></span>
<span data-ttu-id="a1500-103">Yeni-AzStorageAccountManagementPolicyRule 'ta kullanılabilen bir ManagementPolicy kural filtresi nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a1500-103">Creates a ManagementPolicy rule filter object, which can be used in New-AzStorageAccountManagementPolicyRule.</span></span>

## <span data-ttu-id="a1500-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a1500-104">SYNTAX</span></span>

```
New-AzStorageAccountManagementPolicyFilter [-PrefixMatch <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a1500-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a1500-105">DESCRIPTION</span></span>
<span data-ttu-id="a1500-106">**New-AzStorageAccountManagementPolicyFilter** cmdlet 'ı, yeni-azstorageaccountmanagementpolicyrule 'da kullanılabilen bir managementpolicy kural filtresi nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a1500-106">The **New-AzStorageAccountManagementPolicyFilter** cmdlet creates a ManagementPolicy rule filter object, which can be used in New-AzStorageAccountManagementPolicyRule.</span></span>

## <span data-ttu-id="a1500-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a1500-107">EXAMPLES</span></span>

### <span data-ttu-id="a1500-108">Örnek 1: yönetim ilkesi kuralı filtre nesnesi oluşturur, ardından bunu bir yönetim ilkesi kuralına ekleyin ve depolama hesabına ayarlayın</span><span class="sxs-lookup"><span data-stu-id="a1500-108">Example 1: Creates a ManagementPolicy rule filter object, then add it to a management policy rule and set to a Storage account</span></span>
```
PS C:\>$filter = New-AzStorageAccountManagementPolicyFilter -PrefixMatch blobprefix1,blobprefix2
PS C:\>$filter 

PrefixMatch                BlobTypes  
-----------                ---------  
{blobprefix1, blobprefix2} {blockBlob}

PS C:\>$action = Add-AzStorageAccountManagementPolicyAction -BaseBlobAction Delete -daysAfterModificationGreaterThan 100
PS C:\>$rule = New-AzStorageAccountManagementPolicyRule -Name Test -Action $action -Filter $filter
PS C:\>$policy = Set-AzStorageAccountManagementPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -Rule $rule
```

<span data-ttu-id="a1500-109">Bu komut, bir ManagementPolicy kural filtresi nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a1500-109">This command create a ManagementPolicy rule filter object.</span></span> <span data-ttu-id="a1500-110">Ardından bunu bir yönetim ilkesi kuralına ekleyin ve depolama hesabına ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="a1500-110">Then add it to a management policy rule and set to a Storage account.</span></span>

## <span data-ttu-id="a1500-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a1500-111">PARAMETERS</span></span>

### <span data-ttu-id="a1500-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1500-112">-DefaultProfile</span></span>
<span data-ttu-id="a1500-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a1500-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a1500-114">-PrefixMatch</span><span class="sxs-lookup"><span data-stu-id="a1500-114">-PrefixMatch</span></span>
<span data-ttu-id="a1500-115">Öneklerle eşleşecek dizeler dizisi.</span><span class="sxs-lookup"><span data-stu-id="a1500-115">An array of strings for prefixes to be match.</span></span>
<span data-ttu-id="a1500-116">Önek dizesi bir kapsayıcı adıyla başlamalıdır.</span><span class="sxs-lookup"><span data-stu-id="a1500-116">A prefix string must start with a container name.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1500-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1500-117">CommonParameters</span></span>
<span data-ttu-id="a1500-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a1500-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1500-119">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1500-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1500-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a1500-120">INPUTS</span></span>

### <span data-ttu-id="a1500-121">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="a1500-121">None</span></span>

## <span data-ttu-id="a1500-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a1500-122">OUTPUTS</span></span>

### <span data-ttu-id="a1500-123">Microsoft. Azure. Commands. Management. Storage. model. PSManagementPolicyRuleFilter</span><span class="sxs-lookup"><span data-stu-id="a1500-123">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyRuleFilter</span></span>

## <span data-ttu-id="a1500-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a1500-124">NOTES</span></span>

## <span data-ttu-id="a1500-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a1500-125">RELATED LINKS</span></span>
