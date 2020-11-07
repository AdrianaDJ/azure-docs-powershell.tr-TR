---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 15CAC050-F2E9-4872-88E7-516A6D194FAB
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmbootdiagnosticsdata
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMBootDiagnosticsData.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMBootDiagnosticsData.md
ms.openlocfilehash: ab7bae5430bf2b588997d57e92a18a4408ca4334
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93937036"
---
# <span data-ttu-id="50cf3-101">Get-AzVMBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="50cf3-101">Get-AzVMBootDiagnosticsData</span></span>

## <span data-ttu-id="50cf3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="50cf3-102">SYNOPSIS</span></span>
<span data-ttu-id="50cf3-103">Sanal makine için önyükleme tanılama verilerini alır.</span><span class="sxs-lookup"><span data-stu-id="50cf3-103">Gets boot diagnostics data for a virtual machine.</span></span>

## <span data-ttu-id="50cf3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="50cf3-104">SYNTAX</span></span>

### <span data-ttu-id="50cf3-105">WindowsParamSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="50cf3-105">WindowsParamSet (Default)</span></span>
```
Get-AzVMBootDiagnosticsData [-ResourceGroupName] <String> [-Name] <String> [-Windows]
 [-LocalPath] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="50cf3-106">LinuxParamSet</span><span class="sxs-lookup"><span data-stu-id="50cf3-106">LinuxParamSet</span></span>
```
Get-AzVMBootDiagnosticsData [-ResourceGroupName] <String> [-Name] <String> [-Linux]
 [[-LocalPath] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="50cf3-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="50cf3-107">DESCRIPTION</span></span>
<span data-ttu-id="50cf3-108">**Get-AzVMBootDiagnosticsData** cmdlet 'i sanal makine için önyükleme tanılama verilerini alır.</span><span class="sxs-lookup"><span data-stu-id="50cf3-108">The **Get-AzVMBootDiagnosticsData** cmdlet gets boot diagnostics data for a virtual machine.</span></span>

## <span data-ttu-id="50cf3-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="50cf3-109">EXAMPLES</span></span>

### <span data-ttu-id="50cf3-110">Örnek 1: önyükleme tanılama verilerini alma</span><span class="sxs-lookup"><span data-stu-id="50cf3-110">Example 1: Get boot diagnostics data</span></span>
```
PS C:\> Get-AzVMBootDiagnosticsData -ResourceGroupName "ResourceGroup11" -Name "ContosoVM07" -Windows -LocalPath "C:\Contoso\BootDiagnostics"
```

<span data-ttu-id="50cf3-111">Bu komut, ContosoVM07 adındaki sanal makine için önyükleme tanılama verilerini alır.</span><span class="sxs-lookup"><span data-stu-id="50cf3-111">This command gets boot diagnostics data for the virtual machine named ContosoVM07.</span></span>
<span data-ttu-id="50cf3-112">Bu sanal makine Windows işletim sistemini çalıştırır.</span><span class="sxs-lookup"><span data-stu-id="50cf3-112">This virtual machine runs the Windows operating system.</span></span>
<span data-ttu-id="50cf3-113">Komut, verileri belirtilen yerel yolda depolar.</span><span class="sxs-lookup"><span data-stu-id="50cf3-113">The command stores the data in specified local path.</span></span>

## <span data-ttu-id="50cf3-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="50cf3-114">PARAMETERS</span></span>

### <span data-ttu-id="50cf3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50cf3-115">-DefaultProfile</span></span>
<span data-ttu-id="50cf3-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="50cf3-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="50cf3-117">-Linux</span><span class="sxs-lookup"><span data-stu-id="50cf3-117">-Linux</span></span>
<span data-ttu-id="50cf3-118">Sanal makinenin Linux işletim sistemini yürüttüğünde emin olmak.</span><span class="sxs-lookup"><span data-stu-id="50cf3-118">Indicates that the virtual machine runs the Linux operating system.</span></span>

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

### <span data-ttu-id="50cf3-119">-LocalPath</span><span class="sxs-lookup"><span data-stu-id="50cf3-119">-LocalPath</span></span>
<span data-ttu-id="50cf3-120">Önyükleme Tanılama verileri için yerel yolu belirtir.</span><span class="sxs-lookup"><span data-stu-id="50cf3-120">Specifies the local path for the boot diagnostics data.</span></span>

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

### <span data-ttu-id="50cf3-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="50cf3-121">-Name</span></span>
<span data-ttu-id="50cf3-122">Bu cmdlet 'in tanılama verilerini aldığı sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="50cf3-122">Specifies the name of the virtual machine for which this cmdlet gets diagnostics data.</span></span>

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

### <span data-ttu-id="50cf3-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50cf3-123">-ResourceGroupName</span></span>
<span data-ttu-id="50cf3-124">Sanal makinenin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="50cf3-124">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="50cf3-125">-Windows</span><span class="sxs-lookup"><span data-stu-id="50cf3-125">-Windows</span></span>
<span data-ttu-id="50cf3-126">Sanal makinenin Windows işletim sistemini yürüttüi gösterir.</span><span class="sxs-lookup"><span data-stu-id="50cf3-126">Indicates that the virtual machine runs the Windows operating system.</span></span>

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

### <span data-ttu-id="50cf3-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50cf3-127">CommonParameters</span></span>
<span data-ttu-id="50cf3-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="50cf3-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50cf3-129">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50cf3-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50cf3-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="50cf3-130">INPUTS</span></span>

### <span data-ttu-id="50cf3-131">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="50cf3-131">None</span></span>
<span data-ttu-id="50cf3-132">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="50cf3-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="50cf3-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="50cf3-133">OUTPUTS</span></span>

### <span data-ttu-id="50cf3-134">Microsoft. Azure. Commands. COMPUTE. modeller. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="50cf3-134">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="50cf3-135">Microsoft. Azure. Commands. COMPUTE. modeller. Psvirtualmachineınstanceview</span><span class="sxs-lookup"><span data-stu-id="50cf3-135">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineInstanceView</span></span>

## <span data-ttu-id="50cf3-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="50cf3-136">NOTES</span></span>

## <span data-ttu-id="50cf3-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="50cf3-137">RELATED LINKS</span></span>

[<span data-ttu-id="50cf3-138">Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="50cf3-138">Set-AzVMBootDiagnostic</span></span>](./Set-AzVMBootDiagnostic.md)


