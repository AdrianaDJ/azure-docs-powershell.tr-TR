---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzDiskEncryptionSetAssociatedResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzDiskEncryptionSetAssociatedResource.md
ms.openlocfilehash: f85b1ffb181a277e750d6f6f4a67ef55ad2a75bc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94324805"
---
# <span data-ttu-id="5edf9-101">Get-AzDiskEncryptionSetAssociatedResource</span><span class="sxs-lookup"><span data-stu-id="5edf9-101">Get-AzDiskEncryptionSetAssociatedResource</span></span>

## <span data-ttu-id="5edf9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5edf9-102">SYNOPSIS</span></span>
<span data-ttu-id="5edf9-103">Belirtilen disk şifrelemesi kümesiyle ilişkili kaynakların listesini alır.</span><span class="sxs-lookup"><span data-stu-id="5edf9-103">Gets the list of resources associated with the specified disk encryption set.</span></span>

## <span data-ttu-id="5edf9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5edf9-104">SYNTAX</span></span>

```
Get-AzDiskEncryptionSetAssociatedResource [-ResourceGroupName] <String> [-DiskEncryptionSetName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5edf9-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="5edf9-105">DESCRIPTION</span></span>
<span data-ttu-id="5edf9-106">**Get-Azdiskencryptionsetassociilenkaynak** cmdlet 'i, belirtilen disk şifrelemesi kümesiyle ilişkili kaynakların listesini alır.</span><span class="sxs-lookup"><span data-stu-id="5edf9-106">The **Get-AzDiskEncryptionSetAssociatedResource** cmdlet gets the list of resources associated with the specified disk encryption set.</span></span>

## <span data-ttu-id="5edf9-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5edf9-107">EXAMPLES</span></span>

### <span data-ttu-id="5edf9-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="5edf9-108">Example 1</span></span>
```powershell
PS C:\> Get-AzDiskEncryptionSetAssociatedResource -ResourceGroupName $RGname -DiskEncryptionSetName $diskEncryptionSetName

/subscriptions/xxxxx-xxx-xx/resourceGroups/exampleResourceGroup/providers/Microsoft.Compute/disks/exampleDisk01
/subscriptions/xxxxx-xxx-xx/resourceGroups/exampleResourceGroup/providers/Microsoft.Compute/disks/exmapleDisk02
```

<span data-ttu-id="5edf9-109">Cmdlet, sağlanan disk şifrelemesi kümesiyle ilişkilendirilmiş olan ' exampleDisk01 ' ve ' exampleDisk02 ' adlı iki kaynağı alır</span><span class="sxs-lookup"><span data-stu-id="5edf9-109">The cmdlet retrieves the two resources, 'exampleDisk01' and 'exampleDisk02', associated with the provided Disk Encryption Set</span></span>

## <span data-ttu-id="5edf9-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5edf9-110">PARAMETERS</span></span>

### <span data-ttu-id="5edf9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5edf9-111">-DefaultProfile</span></span>
<span data-ttu-id="5edf9-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5edf9-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5edf9-113">-DiskEncryptionSetName</span><span class="sxs-lookup"><span data-stu-id="5edf9-113">-DiskEncryptionSetName</span></span>
<span data-ttu-id="5edf9-114">Disk şifreleme kümesi adı.</span><span class="sxs-lookup"><span data-stu-id="5edf9-114">Name of disk encryption set.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5edf9-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5edf9-115">-ResourceGroupName</span></span>
<span data-ttu-id="5edf9-116">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5edf9-116">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5edf9-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5edf9-117">CommonParameters</span></span>
<span data-ttu-id="5edf9-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5edf9-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5edf9-119">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="5edf9-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5edf9-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5edf9-120">INPUTS</span></span>

### <span data-ttu-id="5edf9-121">System. String</span><span class="sxs-lookup"><span data-stu-id="5edf9-121">System.String</span></span>

## <span data-ttu-id="5edf9-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5edf9-122">OUTPUTS</span></span>

### <span data-ttu-id="5edf9-123">System. Uri []</span><span class="sxs-lookup"><span data-stu-id="5edf9-123">System.Uri[]</span></span>

## <span data-ttu-id="5edf9-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5edf9-124">NOTES</span></span>

## <span data-ttu-id="5edf9-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5edf9-125">RELATED LINKS</span></span>
