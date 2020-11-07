---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 15CAC050-F2E9-4872-88E7-516A6D194FAB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmbootdiagnosticsdata
schema: 2.0.0
ms.openlocfilehash: 867f2c14e90eddd9649e0720d41f56aa896c61ff
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939170"
---
# <span data-ttu-id="6daf1-101">Get-AzureRmVMBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="6daf1-101">Get-AzureRmVMBootDiagnosticsData</span></span>

## <span data-ttu-id="6daf1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6daf1-102">SYNOPSIS</span></span>
<span data-ttu-id="6daf1-103">Sanal makine için önyükleme tanılama verilerini alır.</span><span class="sxs-lookup"><span data-stu-id="6daf1-103">Gets boot diagnostics data for a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6daf1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6daf1-104">SYNTAX</span></span>

### <span data-ttu-id="6daf1-105">WindowsParamSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="6daf1-105">WindowsParamSet (Default)</span></span>
```
Get-AzureRmVMBootDiagnosticsData [-ResourceGroupName] <String> [-Name] <String> [-Windows]
 [-LocalPath] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6daf1-106">LinuxParamSet</span><span class="sxs-lookup"><span data-stu-id="6daf1-106">LinuxParamSet</span></span>
```
Get-AzureRmVMBootDiagnosticsData [-ResourceGroupName] <String> [-Name] <String> [-Linux]
 [[-LocalPath] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6daf1-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="6daf1-107">DESCRIPTION</span></span>
<span data-ttu-id="6daf1-108">**Get-AzureRmVMBootDiagnosticsData** cmdlet 'i sanal makine için önyükleme tanılama verilerini alır.</span><span class="sxs-lookup"><span data-stu-id="6daf1-108">The **Get-AzureRmVMBootDiagnosticsData** cmdlet gets boot diagnostics data for a virtual machine.</span></span>

## <span data-ttu-id="6daf1-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6daf1-109">EXAMPLES</span></span>

### <span data-ttu-id="6daf1-110">Örnek 1: önyükleme tanılama verilerini alma</span><span class="sxs-lookup"><span data-stu-id="6daf1-110">Example 1: Get boot diagnostics data</span></span>
```
PS C:\> Get-AzureRmVMBootDiagnosticsData -ResourceGroupName "ResourceGroup11" -Name "ContosoVM07" -Windows -LocalPath "C:\Contoso\BootDiagnostics"
```

<span data-ttu-id="6daf1-111">Bu komut, ContosoVM07 adındaki sanal makine için önyükleme tanılama verilerini alır.</span><span class="sxs-lookup"><span data-stu-id="6daf1-111">This command gets boot diagnostics data for the virtual machine named ContosoVM07.</span></span>
<span data-ttu-id="6daf1-112">Bu sanal makine Windows işletim sistemini çalıştırır.</span><span class="sxs-lookup"><span data-stu-id="6daf1-112">This virtual machine runs the Windows operating system.</span></span>
<span data-ttu-id="6daf1-113">Komut, verileri belirtilen yerel yolda depolar.</span><span class="sxs-lookup"><span data-stu-id="6daf1-113">The command stores the data in specified local path.</span></span>

## <span data-ttu-id="6daf1-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6daf1-114">PARAMETERS</span></span>

### <span data-ttu-id="6daf1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6daf1-115">-DefaultProfile</span></span>
<span data-ttu-id="6daf1-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6daf1-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6daf1-117">-Linux</span><span class="sxs-lookup"><span data-stu-id="6daf1-117">-Linux</span></span>
<span data-ttu-id="6daf1-118">Sanal makinenin Linux işletim sistemini yürüttüğünde emin olmak.</span><span class="sxs-lookup"><span data-stu-id="6daf1-118">Indicates that the virtual machine runs the Linux operating system.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: LinuxParamSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6daf1-119">-LocalPath</span><span class="sxs-lookup"><span data-stu-id="6daf1-119">-LocalPath</span></span>
<span data-ttu-id="6daf1-120">Önyükleme Tanılama verileri için yerel yolu belirtir.</span><span class="sxs-lookup"><span data-stu-id="6daf1-120">Specifies the local path for the boot diagnostics data.</span></span>

```yaml
Type: String
Parameter Sets: WindowsParamSet
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: LinuxParamSet
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6daf1-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="6daf1-121">-Name</span></span>
<span data-ttu-id="6daf1-122">Bu cmdlet 'in tanılama verilerini aldığı sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6daf1-122">Specifies the name of the virtual machine for which this cmdlet gets diagnostics data.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6daf1-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6daf1-123">-ResourceGroupName</span></span>
<span data-ttu-id="6daf1-124">Sanal makinenin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6daf1-124">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="6daf1-125">-Windows</span><span class="sxs-lookup"><span data-stu-id="6daf1-125">-Windows</span></span>
<span data-ttu-id="6daf1-126">Sanal makinenin Windows işletim sistemini yürüttüi gösterir.</span><span class="sxs-lookup"><span data-stu-id="6daf1-126">Indicates that the virtual machine runs the Windows operating system.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: WindowsParamSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6daf1-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6daf1-127">CommonParameters</span></span>
<span data-ttu-id="6daf1-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6daf1-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6daf1-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6daf1-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6daf1-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6daf1-130">INPUTS</span></span>

### <span data-ttu-id="6daf1-131">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="6daf1-131">None</span></span>
<span data-ttu-id="6daf1-132">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="6daf1-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6daf1-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6daf1-133">OUTPUTS</span></span>

### <span data-ttu-id="6daf1-134">Microsoft. Azure. Commands. COMPUTE. modeller. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="6daf1-134">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="6daf1-135">Microsoft. Azure. Commands. COMPUTE. modeller. Psvirtualmachineınstanceview</span><span class="sxs-lookup"><span data-stu-id="6daf1-135">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineInstanceView</span></span>

## <span data-ttu-id="6daf1-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6daf1-136">NOTES</span></span>

## <span data-ttu-id="6daf1-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6daf1-137">RELATED LINKS</span></span>

[<span data-ttu-id="6daf1-138">Set-AzureRmVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="6daf1-138">Set-AzureRmVMBootDiagnostics</span></span>](./Set-AzureRmVMBootDiagnostics.md)


