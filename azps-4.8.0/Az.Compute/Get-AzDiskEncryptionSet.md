---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azdiskencryptionset.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzDiskEncryptionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzDiskEncryptionSet.md
ms.openlocfilehash: 7d2b23c08f7ce910daf87f7cebbea844d5bda6f0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94108147"
---
# <span data-ttu-id="c0528-101">Get-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="c0528-101">Get-AzDiskEncryptionSet</span></span>

## <span data-ttu-id="c0528-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c0528-102">SYNOPSIS</span></span>
<span data-ttu-id="c0528-103">Disk şifreleme kümelerini alma veya listeleme.</span><span class="sxs-lookup"><span data-stu-id="c0528-103">Get or list disk encryption sets.</span></span>

## <span data-ttu-id="c0528-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c0528-104">SYNTAX</span></span>

```
Get-AzDiskEncryptionSet [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c0528-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c0528-105">DESCRIPTION</span></span>
<span data-ttu-id="c0528-106">Disk şifreleme kümelerini alma veya listeleme.</span><span class="sxs-lookup"><span data-stu-id="c0528-106">Get or list disk encryption sets.</span></span>

## <span data-ttu-id="c0528-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c0528-107">EXAMPLES</span></span>

### <span data-ttu-id="c0528-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="c0528-108">Example 1</span></span>
```powershell
PS C:\> Get-AzDiskEncryptionSet -ResourceGroupName rg1 -Name enc1;

ResourceGroupName : rg1
Identity          : Microsoft.Azure.Management.Compute.Models.EncryptionSetIdentity
ActiveKey         : Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference
PreviousKeys      : {}
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.Compute/diskEncryptionSets/enc1
Name              : enc1
Type              : Microsoft.Compute/diskEncryptionSets
Location          : westcentralus
Tags              : {}
```

<span data-ttu-id="c0528-109">' Enc1 ' disk şifrelemesi kümesini alma</span><span class="sxs-lookup"><span data-stu-id="c0528-109">Get disk encryption set 'enc1'</span></span>

### <span data-ttu-id="c0528-110">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="c0528-110">Example 2</span></span>
```powershell
PS C:\> Get-AzDiskEncryptionSet

ResourceGroupName : rg1
Identity          : Microsoft.Azure.Management.Compute.Models.EncryptionSetIdentity
ActiveKey         : Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference
PreviousKeys      : {}
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.Compute/diskEncryptionSets/enc1
Name              : enc1
Type              : Microsoft.Compute/diskEncryptionSets
Location          : westcentralus
Tags              : {}

ResourceGroupName : rg1
Identity          : Microsoft.Azure.Management.Compute.Models.EncryptionSetIdentity
ActiveKey         : Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference
PreviousKeys      : {}
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.Compute/diskEncryptionSets/enc2
Name              : enc2
Type              : Microsoft.Compute/diskEncryptionSets
Location          : westcentralus
Tags              : {}
```

<span data-ttu-id="c0528-111">' RG1 ' kaynak grubundaki tüm disk şifreleme kümelerini alın.</span><span class="sxs-lookup"><span data-stu-id="c0528-111">Get all disk encryption sets in resource group 'rg1'.</span></span>

### <span data-ttu-id="c0528-112">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="c0528-112">Example 3</span></span>
```powershell
PS C:\> Get-AzDiskEncryptionSet -ResourceGroupName rg1

ResourceGroupName : rg1
Identity          : Microsoft.Azure.Management.Compute.Models.EncryptionSetIdentity
ActiveKey         : Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference
PreviousKeys      : {}
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.Compute/diskEncryptionSets/enc1
Name              : enc1
Type              : Microsoft.Compute/diskEncryptionSets
Location          : westcentralus
Tags              : {}

ResourceGroupName : rg1
Identity          : Microsoft.Azure.Management.Compute.Models.EncryptionSetIdentity
ActiveKey         : Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference
PreviousKeys      : {}
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.Compute/diskEncryptionSets/enc2
Name              : enc2
Type              : Microsoft.Compute/diskEncryptionSets
Location          : westcentralus
Tags              : {}

ResourceGroupName : rg2
Identity          : Microsoft.Azure.Management.Compute.Models.EncryptionSetIdentity
ActiveKey         : Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference
PreviousKeys      : {}
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.Compute/diskEncryptionSets/enc3
Name              : enc3
Type              : Microsoft.Compute/diskEncryptionSets
Location          : westcentralus
Tags              : {}
```

<span data-ttu-id="c0528-113">Tüm disk şifreleme kümelerini abonelikle edinin.</span><span class="sxs-lookup"><span data-stu-id="c0528-113">Get all disk encryption sets in subscription.</span></span>

## <span data-ttu-id="c0528-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c0528-114">PARAMETERS</span></span>

### <span data-ttu-id="c0528-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0528-115">-DefaultProfile</span></span>
<span data-ttu-id="c0528-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c0528-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c0528-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="c0528-117">-Name</span></span>
<span data-ttu-id="c0528-118">Disk şifreleme kümesi adı.</span><span class="sxs-lookup"><span data-stu-id="c0528-118">Name of disk encryption set.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DiskEncryptionSetName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0528-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0528-119">-ResourceGroupName</span></span>
<span data-ttu-id="c0528-120">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c0528-120">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0528-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0528-121">CommonParameters</span></span>
<span data-ttu-id="c0528-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c0528-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0528-123">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="c0528-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0528-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c0528-124">INPUTS</span></span>

### <span data-ttu-id="c0528-125">System. String</span><span class="sxs-lookup"><span data-stu-id="c0528-125">System.String</span></span>

## <span data-ttu-id="c0528-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c0528-126">OUTPUTS</span></span>

### <span data-ttu-id="c0528-127">Microsoft.Azure.Commands.Compute.Automation.Models.PSDıskencryptionset</span><span class="sxs-lookup"><span data-stu-id="c0528-127">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span></span>

## <span data-ttu-id="c0528-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c0528-128">NOTES</span></span>

## <span data-ttu-id="c0528-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c0528-129">RELATED LINKS</span></span>
