---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 15CAC050-F2E9-4872-88E7-516A6D194FAB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmbootdiagnosticsdata
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMBootDiagnosticsData.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMBootDiagnosticsData.md
ms.openlocfilehash: 9d8da69f401f17aa757d5bb5e152f1557ee5356a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763463"
---
# <span data-ttu-id="df403-101">Get-AzureRmVMBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="df403-101">Get-AzureRmVMBootDiagnosticsData</span></span>

## <span data-ttu-id="df403-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="df403-102">SYNOPSIS</span></span>
<span data-ttu-id="df403-103">Sanal makine için önyükleme tanılama verilerini alır.</span><span class="sxs-lookup"><span data-stu-id="df403-103">Gets boot diagnostics data for a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="df403-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="df403-104">SYNTAX</span></span>

### <span data-ttu-id="df403-105">WindowsParamSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="df403-105">WindowsParamSet (Default)</span></span>
```
Get-AzureRmVMBootDiagnosticsData [-ResourceGroupName] <String> [-Name] <String> [-Windows]
 [-LocalPath] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="df403-106">LinuxParamSet</span><span class="sxs-lookup"><span data-stu-id="df403-106">LinuxParamSet</span></span>
```
Get-AzureRmVMBootDiagnosticsData [-ResourceGroupName] <String> [-Name] <String> [-Linux]
 [[-LocalPath] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="df403-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="df403-107">DESCRIPTION</span></span>
<span data-ttu-id="df403-108">**Get-AzureRmVMBootDiagnosticsData** cmdlet 'i sanal makine için önyükleme tanılama verilerini alır.</span><span class="sxs-lookup"><span data-stu-id="df403-108">The **Get-AzureRmVMBootDiagnosticsData** cmdlet gets boot diagnostics data for a virtual machine.</span></span>

## <span data-ttu-id="df403-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="df403-109">EXAMPLES</span></span>

### <span data-ttu-id="df403-110">Örnek 1: önyükleme tanılama verilerini alma</span><span class="sxs-lookup"><span data-stu-id="df403-110">Example 1: Get boot diagnostics data</span></span>
```
PS C:\> Get-AzureRmVMBootDiagnosticsData -ResourceGroupName "ResourceGroup11" -Name "ContosoVM07" -Windows -LocalPath "C:\Contoso\BootDiagnostics"
```

<span data-ttu-id="df403-111">Bu komut, ContosoVM07 adındaki sanal makine için önyükleme tanılama verilerini alır.</span><span class="sxs-lookup"><span data-stu-id="df403-111">This command gets boot diagnostics data for the virtual machine named ContosoVM07.</span></span>
<span data-ttu-id="df403-112">Bu sanal makine Windows işletim sistemini çalıştırır.</span><span class="sxs-lookup"><span data-stu-id="df403-112">This virtual machine runs the Windows operating system.</span></span>
<span data-ttu-id="df403-113">Komut, verileri belirtilen yerel yolda depolar.</span><span class="sxs-lookup"><span data-stu-id="df403-113">The command stores the data in specified local path.</span></span>

## <span data-ttu-id="df403-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="df403-114">PARAMETERS</span></span>

### <span data-ttu-id="df403-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df403-115">-DefaultProfile</span></span>
<span data-ttu-id="df403-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="df403-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="df403-117">-Linux</span><span class="sxs-lookup"><span data-stu-id="df403-117">-Linux</span></span>
<span data-ttu-id="df403-118">Sanal makinenin Linux işletim sistemini yürüttüğünde emin olmak.</span><span class="sxs-lookup"><span data-stu-id="df403-118">Indicates that the virtual machine runs the Linux operating system.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: LinuxParamSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df403-119">-LocalPath</span><span class="sxs-lookup"><span data-stu-id="df403-119">-LocalPath</span></span>
<span data-ttu-id="df403-120">Önyükleme Tanılama verileri için yerel yolu belirtir.</span><span class="sxs-lookup"><span data-stu-id="df403-120">Specifies the local path for the boot diagnostics data.</span></span>

```yaml
Type: System.String
Parameter Sets: WindowsParamSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: LinuxParamSet
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df403-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="df403-121">-Name</span></span>
<span data-ttu-id="df403-122">Bu cmdlet 'in tanılama verilerini aldığı sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="df403-122">Specifies the name of the virtual machine for which this cmdlet gets diagnostics data.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df403-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df403-123">-ResourceGroupName</span></span>
<span data-ttu-id="df403-124">Sanal makinenin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="df403-124">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df403-125">-Windows</span><span class="sxs-lookup"><span data-stu-id="df403-125">-Windows</span></span>
<span data-ttu-id="df403-126">Sanal makinenin Windows işletim sistemini yürüttüi gösterir.</span><span class="sxs-lookup"><span data-stu-id="df403-126">Indicates that the virtual machine runs the Windows operating system.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WindowsParamSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df403-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df403-127">CommonParameters</span></span>
<span data-ttu-id="df403-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="df403-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df403-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df403-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df403-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="df403-130">INPUTS</span></span>

### <span data-ttu-id="df403-131">System. String</span><span class="sxs-lookup"><span data-stu-id="df403-131">System.String</span></span>

## <span data-ttu-id="df403-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="df403-132">OUTPUTS</span></span>

### <span data-ttu-id="df403-133">Microsoft. Azure. Commands. COMPUTE. modeller. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="df403-133">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="df403-134">Microsoft. Azure. Commands. COMPUTE. modeller. Psvirtualmachineınstanceview</span><span class="sxs-lookup"><span data-stu-id="df403-134">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineInstanceView</span></span>

## <span data-ttu-id="df403-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="df403-135">NOTES</span></span>

## <span data-ttu-id="df403-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="df403-136">RELATED LINKS</span></span>

[<span data-ttu-id="df403-137">Set-AzureRmVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="df403-137">Set-AzureRmVMBootDiagnostics</span></span>](./Set-AzureRmVMBootDiagnostics.md)


