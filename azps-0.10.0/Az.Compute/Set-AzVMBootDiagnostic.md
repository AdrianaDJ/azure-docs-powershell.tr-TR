---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 9A6F140C-9F1C-4701-9603-FC6107FCAF92
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmbootdiagnostics
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMBootDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMBootDiagnostic.md
ms.openlocfilehash: e3e03083e831f38143423e69c84a67bfbc0440db
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936844"
---
# <span data-ttu-id="82527-101">Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="82527-101">Set-AzVMBootDiagnostic</span></span>

## <span data-ttu-id="82527-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="82527-102">SYNOPSIS</span></span>
<span data-ttu-id="82527-103">Sanal makinenin önyükleme tanılaması özelliklerini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="82527-103">Modifies boot diagnostics properties of a virtual machine.</span></span>

## <span data-ttu-id="82527-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="82527-104">SYNTAX</span></span>

### <span data-ttu-id="82527-105">EnableBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="82527-105">EnableBootDiagnostics</span></span>
```
Set-AzVMBootDiagnostic [-VM] <PSVirtualMachine> [-Enable] [-ResourceGroupName] <String>
 [[-StorageAccountName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="82527-106">DisableBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="82527-106">DisableBootDiagnostics</span></span>
```
Set-AzVMBootDiagnostic [-VM] <PSVirtualMachine> [-Disable] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="82527-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="82527-107">DESCRIPTION</span></span>
<span data-ttu-id="82527-108">**Set-AzVMBootDiagnostic** cmdlet 'i sanal makinenin önyükleme tanılaması özelliklerini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="82527-108">The **Set-AzVMBootDiagnostic** cmdlet modifies boot diagnostics properties of a virtual machine.</span></span>

## <span data-ttu-id="82527-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="82527-109">EXAMPLES</span></span>

### <span data-ttu-id="82527-110">Örnek 1: önyükleme tanılamayı etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="82527-110">Example 1: Enable boot diagnostics</span></span>
```
PS C:\> $VM = Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "ContosoVM07"
PS C:\> Set-AzVMBootDiagnostic -VM $VM -Enable -ResourceGroupName "ResourceGroup11" -StorageAccountName "DiagnosticStorage"
```

<span data-ttu-id="82527-111">İlk komut ContosoVM07 adındaki sanal makineyi **Get-AzVM** kullanarak alır.</span><span class="sxs-lookup"><span data-stu-id="82527-111">The first command gets the virtual machine named ContosoVM07 by using **Get-AzVM**.</span></span>
<span data-ttu-id="82527-112">Komut, $VM değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="82527-112">The command stores it in the $VM variable.</span></span>

<span data-ttu-id="82527-113">İkinci komut $VM sanal makinesi için önyükleme tanılaması 'nı mümkün kılar.</span><span class="sxs-lookup"><span data-stu-id="82527-113">The second command enables boot diagnostics for the virtual machine in $VM.</span></span>
<span data-ttu-id="82527-114">Tanılama verileri belirtilen hesapta depolanır.</span><span class="sxs-lookup"><span data-stu-id="82527-114">Diagnostics data is stored in the specified account.</span></span>

## <span data-ttu-id="82527-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="82527-115">PARAMETERS</span></span>

### <span data-ttu-id="82527-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82527-116">-DefaultProfile</span></span>
<span data-ttu-id="82527-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="82527-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="82527-118">-Devre dışı bırak</span><span class="sxs-lookup"><span data-stu-id="82527-118">-Disable</span></span>
<span data-ttu-id="82527-119">Bu cmdlet 'in sanal makinenin önyükleme tanılamasını devre dışı bırakacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="82527-119">Indicates that this cmdlet disables the boot diagnostics for the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: DisableBootDiagnostics
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82527-120">-Enable</span><span class="sxs-lookup"><span data-stu-id="82527-120">-Enable</span></span>
<span data-ttu-id="82527-121">Bu cmdlet 'in sanal makine için önyükleme tanılamayı etkinleştirdiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="82527-121">Indicates that this cmdlet enables the boot diagnostics for the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: EnableBootDiagnostics
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82527-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82527-122">-ResourceGroupName</span></span>
<span data-ttu-id="82527-123">Sanal makinenin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="82527-123">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: EnableBootDiagnostics
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82527-124">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="82527-124">-StorageAccountName</span></span>
<span data-ttu-id="82527-125">Önyükleme tanılaması verilerinin kaydedileceği depolama hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="82527-125">Specifies the name of the storage account in which to save boot diagnostics data.</span></span>

```yaml
Type: String
Parameter Sets: EnableBootDiagnostics
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82527-126">-VM</span><span class="sxs-lookup"><span data-stu-id="82527-126">-VM</span></span>
<span data-ttu-id="82527-127">Bu cmdlet 'in önyükleme tanılamasını değiştirdiği sanal makineyi belirtir.</span><span class="sxs-lookup"><span data-stu-id="82527-127">Specifies the virtual machine for which this cmdlet changes boot diagnostics.</span></span>
<span data-ttu-id="82527-128">Sanal makine nesnesi edinmek için Get-AzVM cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="82527-128">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>

```yaml
Type: PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="82527-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82527-129">CommonParameters</span></span>
<span data-ttu-id="82527-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="82527-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82527-131">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="82527-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82527-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="82527-132">INPUTS</span></span>

### <span data-ttu-id="82527-133">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="82527-133">PSVirtualMachine</span></span>
<span data-ttu-id="82527-134">' VM ' parametresi ardışık düzene ' PSVirtualMachine ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="82527-134">Parameter 'VM' accepts value of type 'PSVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="82527-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="82527-135">OUTPUTS</span></span>

### <span data-ttu-id="82527-136">Microsoft. Azure. Commands. COMPUTE. modeller. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="82527-136">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="82527-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="82527-137">NOTES</span></span>

## <span data-ttu-id="82527-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="82527-138">RELATED LINKS</span></span>

[<span data-ttu-id="82527-139">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="82527-139">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="82527-140">Get-AzVMBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="82527-140">Get-AzVMBootDiagnosticsData</span></span>](./Get-AzVMBootDiagnosticsData.md)


