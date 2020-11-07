---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermdisk
schema: 2.0.0
ms.openlocfilehash: 5bf1e7cb5a043afaaa4b6fd4d5e8f6820c14fbb1
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939613"
---
# <span data-ttu-id="3bb46-101">Get-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="3bb46-101">Get-AzureRmDisk</span></span>

## <span data-ttu-id="3bb46-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3bb46-102">SYNOPSIS</span></span>
<span data-ttu-id="3bb46-103">Yönetilen diskin özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="3bb46-103">Gets the properties of a Managed disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3bb46-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3bb46-104">SYNTAX</span></span>

```
Get-AzureRmDisk [[-ResourceGroupName] <String>] [[-DiskName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3bb46-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="3bb46-105">DESCRIPTION</span></span>
<span data-ttu-id="3bb46-106">**Get-Azurermdısk** cmdlet 'ı, yönetilen bir diskin özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="3bb46-106">The **Get-AzureRmDisk** cmdlet gets the properties of a Managed disk.</span></span>

## <span data-ttu-id="3bb46-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3bb46-107">EXAMPLES</span></span>

### <span data-ttu-id="3bb46-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="3bb46-108">Example 1</span></span>
```
PS C:\> Get-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01'
```

<span data-ttu-id="3bb46-109">Bu komut, ' ResourceGroup01 ' kaynak grubundaki ' Disk01 ' adındaki diskin özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="3bb46-109">This command gets the properties of the disk named 'Disk01' in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="3bb46-110">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="3bb46-110">Example 2</span></span>
```
PS C:\> Get-AzureRmDisk -ResourceGroupName 'ResourceGroup01'
```

<span data-ttu-id="3bb46-111">Bu komut, ' ResourceGroup01 ' kaynak grubundaki tüm disklerin özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="3bb46-111">This command gets the properties of all disks in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="3bb46-112">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="3bb46-112">Example 3</span></span>
```
PS C:\> Get-AzureRmDisk
```

<span data-ttu-id="3bb46-113">Bu komut, aboneliğin altındaki tüm disklerin özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="3bb46-113">This command gets the properties of all disks under the subscription.</span></span>

## <span data-ttu-id="3bb46-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3bb46-114">PARAMETERS</span></span>

### <span data-ttu-id="3bb46-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3bb46-115">-DefaultProfile</span></span>
<span data-ttu-id="3bb46-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3bb46-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bb46-117">-DiskName</span><span class="sxs-lookup"><span data-stu-id="3bb46-117">-DiskName</span></span>
<span data-ttu-id="3bb46-118">Diskin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3bb46-118">Specifies the name of a disk.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3bb46-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3bb46-119">-ResourceGroupName</span></span>
<span data-ttu-id="3bb46-120">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3bb46-120">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3bb46-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3bb46-121">CommonParameters</span></span>
<span data-ttu-id="3bb46-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3bb46-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3bb46-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3bb46-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3bb46-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3bb46-124">INPUTS</span></span>

### <span data-ttu-id="3bb46-125">System. String</span><span class="sxs-lookup"><span data-stu-id="3bb46-125">System.String</span></span>

## <span data-ttu-id="3bb46-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3bb46-126">OUTPUTS</span></span>

### <span data-ttu-id="3bb46-127">Microsoft.Azure.Commands.Compute.Automation.Models.PSDİsk</span><span class="sxs-lookup"><span data-stu-id="3bb46-127">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="3bb46-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3bb46-128">NOTES</span></span>

## <span data-ttu-id="3bb46-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3bb46-129">RELATED LINKS</span></span>

