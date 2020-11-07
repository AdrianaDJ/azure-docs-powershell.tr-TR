---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/convertto-azurermvmmanageddisk
schema: 2.0.0
ms.openlocfilehash: 563b8acadcf84359af740f504f3b25555a2e45f1
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939807"
---
# <span data-ttu-id="4da6f-101">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="4da6f-101">ConvertTo-AzureRmVMManagedDisk</span></span>

## <span data-ttu-id="4da6f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4da6f-102">SYNOPSIS</span></span>
<span data-ttu-id="4da6f-103">Blob tabanlı diskler içeren bir sanal makineyi yönetilen diskleri olan bir sanal makineye dönüştürür.</span><span class="sxs-lookup"><span data-stu-id="4da6f-103">Converts a virtual machine with blob-based disks to a virtual machine with managed disks.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4da6f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4da6f-104">SYNTAX</span></span>

```
ConvertTo-AzureRmVMManagedDisk [-ResourceGroupName] <String> [-VMName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4da6f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="4da6f-105">DESCRIPTION</span></span>
<span data-ttu-id="4da6f-106">**ConvertTo-AzureRmVMManagedDisk** cmdlet 'i, blob tabanlı disklerdeki sanal makineyi yönetilen diskleri içeren bir sanal makineye dönüştürür.</span><span class="sxs-lookup"><span data-stu-id="4da6f-106">The **ConvertTo-AzureRmVMManagedDisk** cmdlet converts a virtual machine with blob-based disks to a virtual machine with managed disks.</span></span>
<span data-ttu-id="4da6f-107">Bu işlemi çağırmadan önce sanal makinenin durdurulması gerekir.</span><span class="sxs-lookup"><span data-stu-id="4da6f-107">The virtual machine must be stop-deallocated before invoking this operation.</span></span>

## <span data-ttu-id="4da6f-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4da6f-108">EXAMPLES</span></span>

### <span data-ttu-id="4da6f-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="4da6f-109">Example 1</span></span>
```
PS C:\> ConvertTo-AzureRmVMManagedDisk -ResourceGroupName 'ResourceGroup01' -VMName 'VM01'
```

<span data-ttu-id="4da6f-110">Bu komut, ' ResourceGroup01 ' kaynak grubundaki ' VM01 ' adlı sanal makinenin blob tabanlı disklerini yönetilen disklere dönüştürür.</span><span class="sxs-lookup"><span data-stu-id="4da6f-110">This command converts the blob-based disks of the virtual machine named 'VM01' in the resource group 'ResourceGroup01' to managed disks.</span></span>

## <span data-ttu-id="4da6f-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4da6f-111">PARAMETERS</span></span>

### <span data-ttu-id="4da6f-112">-Iş</span><span class="sxs-lookup"><span data-stu-id="4da6f-112">-AsJob</span></span>
<span data-ttu-id="4da6f-113">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="4da6f-113">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4da6f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4da6f-114">-DefaultProfile</span></span>
<span data-ttu-id="4da6f-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4da6f-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4da6f-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4da6f-116">-ResourceGroupName</span></span>
<span data-ttu-id="4da6f-117">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4da6f-117">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4da6f-118">-VMName</span><span class="sxs-lookup"><span data-stu-id="4da6f-118">-VMName</span></span>
<span data-ttu-id="4da6f-119">Sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4da6f-119">Specifies the name of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4da6f-120">-Onay</span><span class="sxs-lookup"><span data-stu-id="4da6f-120">-Confirm</span></span>
<span data-ttu-id="4da6f-121">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4da6f-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4da6f-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4da6f-122">-WhatIf</span></span>
<span data-ttu-id="4da6f-123">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4da6f-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4da6f-124">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="4da6f-124">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4da6f-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4da6f-125">CommonParameters</span></span>
<span data-ttu-id="4da6f-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4da6f-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4da6f-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4da6f-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4da6f-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4da6f-128">INPUTS</span></span>

### <span data-ttu-id="4da6f-129">System. String</span><span class="sxs-lookup"><span data-stu-id="4da6f-129">System.String</span></span>

## <span data-ttu-id="4da6f-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4da6f-130">OUTPUTS</span></span>

### <span data-ttu-id="4da6f-131">System. Object</span><span class="sxs-lookup"><span data-stu-id="4da6f-131">System.Object</span></span>

## <span data-ttu-id="4da6f-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4da6f-132">NOTES</span></span>

## <span data-ttu-id="4da6f-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4da6f-133">RELATED LINKS</span></span>

