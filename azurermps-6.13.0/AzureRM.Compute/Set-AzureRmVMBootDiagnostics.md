---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 9A6F140C-9F1C-4701-9603-FC6107FCAF92
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmbootdiagnostics
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVMBootDiagnostics.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVMBootDiagnostics.md
ms.openlocfilehash: 290c726c53ea4479c4bd1f3cb9b2c607c04f20cc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763890"
---
# <span data-ttu-id="a8137-101">Set-AzureRmVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="a8137-101">Set-AzureRmVMBootDiagnostics</span></span>

## <span data-ttu-id="a8137-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a8137-102">SYNOPSIS</span></span>
<span data-ttu-id="a8137-103">Sanal makinenin önyükleme tanılaması özelliklerini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="a8137-103">Modifies boot diagnostics properties of a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a8137-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a8137-104">SYNTAX</span></span>

### <span data-ttu-id="a8137-105">EnableBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="a8137-105">EnableBootDiagnostics</span></span>
```
Set-AzureRmVMBootDiagnostics [-VM] <PSVirtualMachine> [-Enable] [-ResourceGroupName] <String>
 [[-StorageAccountName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a8137-106">DisableBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="a8137-106">DisableBootDiagnostics</span></span>
```
Set-AzureRmVMBootDiagnostics [-VM] <PSVirtualMachine> [-Disable] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a8137-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="a8137-107">DESCRIPTION</span></span>
<span data-ttu-id="a8137-108">**Set-AzureRmVMBootDiagnostics** cmdlet 'i, sanal makinenin önyükleme tanılaması özelliklerini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="a8137-108">The **Set-AzureRmVMBootDiagnostics** cmdlet modifies boot diagnostics properties of a virtual machine.</span></span>

## <span data-ttu-id="a8137-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a8137-109">EXAMPLES</span></span>

### <span data-ttu-id="a8137-110">Örnek 1: önyükleme tanılamayı etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="a8137-110">Example 1: Enable boot diagnostics</span></span>
```
PS C:\> $VM = Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "ContosoVM07"
PS C:\> Set-AzureRmVMBootDiagnostics -VM $VM -Enable -ResourceGroupName "ResourceGroup11" -StorageAccountName "DiagnosticStorage"
```

<span data-ttu-id="a8137-111">İlk komut ContosoVM07 adındaki sanal makineyi **Get-AzureRmVM** kullanarak alır.</span><span class="sxs-lookup"><span data-stu-id="a8137-111">The first command gets the virtual machine named ContosoVM07 by using **Get-AzureRmVM**.</span></span>
<span data-ttu-id="a8137-112">Komut, $VM değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="a8137-112">The command stores it in the $VM variable.</span></span>
<span data-ttu-id="a8137-113">İkinci komut $VM sanal makinesi için önyükleme tanılaması 'nı mümkün kılar.</span><span class="sxs-lookup"><span data-stu-id="a8137-113">The second command enables boot diagnostics for the virtual machine in $VM.</span></span>
<span data-ttu-id="a8137-114">Tanılama verileri belirtilen hesapta depolanır.</span><span class="sxs-lookup"><span data-stu-id="a8137-114">Diagnostics data is stored in the specified account.</span></span>

## <span data-ttu-id="a8137-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a8137-115">PARAMETERS</span></span>

### <span data-ttu-id="a8137-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8137-116">-DefaultProfile</span></span>
<span data-ttu-id="a8137-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a8137-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a8137-118">-Devre dışı bırak</span><span class="sxs-lookup"><span data-stu-id="a8137-118">-Disable</span></span>
<span data-ttu-id="a8137-119">Bu cmdlet 'in sanal makinenin önyükleme tanılamasını devre dışı bırakacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a8137-119">Indicates that this cmdlet disables the boot diagnostics for the virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DisableBootDiagnostics
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8137-120">-Enable</span><span class="sxs-lookup"><span data-stu-id="a8137-120">-Enable</span></span>
<span data-ttu-id="a8137-121">Bu cmdlet 'in sanal makine için önyükleme tanılamayı etkinleştirdiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="a8137-121">Indicates that this cmdlet enables the boot diagnostics for the virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EnableBootDiagnostics
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8137-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8137-122">-ResourceGroupName</span></span>
<span data-ttu-id="a8137-123">Sanal makinenin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a8137-123">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: EnableBootDiagnostics
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8137-124">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="a8137-124">-StorageAccountName</span></span>
<span data-ttu-id="a8137-125">Önyükleme tanılaması verilerinin kaydedileceği depolama hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a8137-125">Specifies the name of the storage account in which to save boot diagnostics data.</span></span>

```yaml
Type: System.String
Parameter Sets: EnableBootDiagnostics
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8137-126">-VM</span><span class="sxs-lookup"><span data-stu-id="a8137-126">-VM</span></span>
<span data-ttu-id="a8137-127">Bu cmdlet 'in önyükleme tanılamasını değiştirdiği sanal makineyi belirtir.</span><span class="sxs-lookup"><span data-stu-id="a8137-127">Specifies the virtual machine for which this cmdlet changes boot diagnostics.</span></span>
<span data-ttu-id="a8137-128">Sanal makine nesnesi edinmek için Get-AzureRmVM cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="a8137-128">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a8137-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8137-129">CommonParameters</span></span>
<span data-ttu-id="a8137-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a8137-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8137-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8137-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8137-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a8137-132">INPUTS</span></span>

### <span data-ttu-id="a8137-133">Microsoft. Azure. Commands. COMPUTE. modeller. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="a8137-133">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="a8137-134">System. String</span><span class="sxs-lookup"><span data-stu-id="a8137-134">System.String</span></span>

## <span data-ttu-id="a8137-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a8137-135">OUTPUTS</span></span>

### <span data-ttu-id="a8137-136">Microsoft. Azure. Commands. COMPUTE. modeller. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="a8137-136">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="a8137-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a8137-137">NOTES</span></span>

## <span data-ttu-id="a8137-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a8137-138">RELATED LINKS</span></span>

[<span data-ttu-id="a8137-139">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="a8137-139">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="a8137-140">Get-AzureRmVMBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="a8137-140">Get-AzureRmVMBootDiagnosticsData</span></span>](./Get-AzureRmVMBootDiagnosticsData.md)


