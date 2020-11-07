---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/convertto-azurermvmmanageddisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/ConvertTo-AzureRmVMManagedDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/ConvertTo-AzureRmVMManagedDisk.md
ms.openlocfilehash: 4aabd2a7b6e8b4b0b9037fc14189a0e14fdf8920
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762798"
---
# <span data-ttu-id="9329a-101">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="9329a-101">ConvertTo-AzureRmVMManagedDisk</span></span>

## <span data-ttu-id="9329a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9329a-102">SYNOPSIS</span></span>
<span data-ttu-id="9329a-103">Blob tabanlı diskler içeren bir sanal makineyi yönetilen diskleri olan bir sanal makineye dönüştürür.</span><span class="sxs-lookup"><span data-stu-id="9329a-103">Converts a virtual machine with blob-based disks to a virtual machine with managed disks.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9329a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9329a-104">SYNTAX</span></span>

```
ConvertTo-AzureRmVMManagedDisk [-ResourceGroupName] <String> [-VMName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9329a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="9329a-105">DESCRIPTION</span></span>
<span data-ttu-id="9329a-106">**ConvertTo-AzureRmVMManagedDisk** cmdlet 'i, blob tabanlı disklerdeki sanal makineyi yönetilen diskleri içeren bir sanal makineye dönüştürür.</span><span class="sxs-lookup"><span data-stu-id="9329a-106">The **ConvertTo-AzureRmVMManagedDisk** cmdlet converts a virtual machine with blob-based disks to a virtual machine with managed disks.</span></span>
<span data-ttu-id="9329a-107">Bu işlemi çağırmadan önce sanal makinenin durdurulması gerekir.</span><span class="sxs-lookup"><span data-stu-id="9329a-107">The virtual machine must be stop-deallocated before invoking this operation.</span></span>

## <span data-ttu-id="9329a-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9329a-108">EXAMPLES</span></span>

### <span data-ttu-id="9329a-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="9329a-109">Example 1</span></span>
```
PS C:\> ConvertTo-AzureRmVMManagedDisk -ResourceGroupName 'ResourceGroup01' -VMName 'VM01'
```

<span data-ttu-id="9329a-110">Bu komut, ' ResourceGroup01 ' kaynak grubundaki ' VM01 ' adlı sanal makinenin blob tabanlı disklerini yönetilen disklere dönüştürür.</span><span class="sxs-lookup"><span data-stu-id="9329a-110">This command converts the blob-based disks of the virtual machine named 'VM01' in the resource group 'ResourceGroup01' to managed disks.</span></span>

## <span data-ttu-id="9329a-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9329a-111">PARAMETERS</span></span>

### <span data-ttu-id="9329a-112">-Iş</span><span class="sxs-lookup"><span data-stu-id="9329a-112">-AsJob</span></span>
<span data-ttu-id="9329a-113">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="9329a-113">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9329a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9329a-114">-DefaultProfile</span></span>
<span data-ttu-id="9329a-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9329a-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9329a-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9329a-116">-ResourceGroupName</span></span>
<span data-ttu-id="9329a-117">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9329a-117">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9329a-118">-VMName</span><span class="sxs-lookup"><span data-stu-id="9329a-118">-VMName</span></span>
<span data-ttu-id="9329a-119">Sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9329a-119">Specifies the name of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9329a-120">-Onay</span><span class="sxs-lookup"><span data-stu-id="9329a-120">-Confirm</span></span>
<span data-ttu-id="9329a-121">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="9329a-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9329a-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9329a-122">-WhatIf</span></span>
<span data-ttu-id="9329a-123">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="9329a-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9329a-124">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="9329a-124">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9329a-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9329a-125">CommonParameters</span></span>
<span data-ttu-id="9329a-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9329a-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9329a-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9329a-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9329a-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9329a-128">INPUTS</span></span>

### <span data-ttu-id="9329a-129">System. String</span><span class="sxs-lookup"><span data-stu-id="9329a-129">System.String</span></span>

## <span data-ttu-id="9329a-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9329a-130">OUTPUTS</span></span>

### <span data-ttu-id="9329a-131">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. Psoperationdurumresponse</span><span class="sxs-lookup"><span data-stu-id="9329a-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="9329a-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9329a-132">NOTES</span></span>

## <span data-ttu-id="9329a-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9329a-133">RELATED LINKS</span></span>
