---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azdisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzDisk.md
ms.openlocfilehash: 1da5ac8a6952e2a03367e84894f2069ba7ff250f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93937053"
---
# <span data-ttu-id="85edc-101">Get-AzDisk</span><span class="sxs-lookup"><span data-stu-id="85edc-101">Get-AzDisk</span></span>

## <span data-ttu-id="85edc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="85edc-102">SYNOPSIS</span></span>
<span data-ttu-id="85edc-103">Yönetilen diskin özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="85edc-103">Gets the properties of a Managed disk.</span></span>

## <span data-ttu-id="85edc-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="85edc-104">SYNTAX</span></span>

```
Get-AzDisk [[-ResourceGroupName] <String>] [[-DiskName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="85edc-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="85edc-105">DESCRIPTION</span></span>
<span data-ttu-id="85edc-106">**Get-Azdısk** cmdlet 'ı, yönetilen bir diskin özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="85edc-106">The **Get-AzDisk** cmdlet gets the properties of a Managed disk.</span></span>

## <span data-ttu-id="85edc-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="85edc-107">EXAMPLES</span></span>

### <span data-ttu-id="85edc-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="85edc-108">Example 1</span></span>
```
PS C:\> Get-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01'
```

<span data-ttu-id="85edc-109">Bu komut, ' ResourceGroup01 ' kaynak grubundaki ' Disk01 ' adındaki diskin özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="85edc-109">This command gets the properties of the disk named 'Disk01' in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="85edc-110">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="85edc-110">Example 2</span></span>
```
PS C:\> Get-AzDisk -ResourceGroupName 'ResourceGroup01'
```

<span data-ttu-id="85edc-111">Bu komut, ' ResourceGroup01 ' kaynak grubundaki tüm disklerin özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="85edc-111">This command gets the properties of all disks in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="85edc-112">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="85edc-112">Example 3</span></span>
```
PS C:\> Get-AzDisk
```

<span data-ttu-id="85edc-113">Bu komut, aboneliğin altındaki tüm disklerin özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="85edc-113">This command gets the properties of all disks under the subscription.</span></span>

## <span data-ttu-id="85edc-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="85edc-114">PARAMETERS</span></span>

### <span data-ttu-id="85edc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85edc-115">-DefaultProfile</span></span>
<span data-ttu-id="85edc-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="85edc-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="85edc-117">-DiskName</span><span class="sxs-lookup"><span data-stu-id="85edc-117">-DiskName</span></span>
<span data-ttu-id="85edc-118">Diskin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="85edc-118">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="85edc-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85edc-119">-ResourceGroupName</span></span>
<span data-ttu-id="85edc-120">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="85edc-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="85edc-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85edc-121">CommonParameters</span></span>
<span data-ttu-id="85edc-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="85edc-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85edc-123">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="85edc-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85edc-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="85edc-124">INPUTS</span></span>

### <span data-ttu-id="85edc-125">System. String</span><span class="sxs-lookup"><span data-stu-id="85edc-125">System.String</span></span>

## <span data-ttu-id="85edc-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="85edc-126">OUTPUTS</span></span>

### <span data-ttu-id="85edc-127">Microsoft.Azure.Commands.Compute.Automation.Models.PSDİsk</span><span class="sxs-lookup"><span data-stu-id="85edc-127">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="85edc-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="85edc-128">NOTES</span></span>

## <span data-ttu-id="85edc-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="85edc-129">RELATED LINKS</span></span>

