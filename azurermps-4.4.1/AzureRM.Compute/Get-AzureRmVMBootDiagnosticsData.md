---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 15CAC050-F2E9-4872-88E7-516A6D194FAB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMBootDiagnosticsData.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMBootDiagnosticsData.md
ms.openlocfilehash: dfe9324644115d00054961e8e159c672d1aba588
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93595201"
---
# <span data-ttu-id="3ed0f-101">Get-AzureRmVMBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="3ed0f-101">Get-AzureRmVMBootDiagnosticsData</span></span>

## <span data-ttu-id="3ed0f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3ed0f-102">SYNOPSIS</span></span>
<span data-ttu-id="3ed0f-103">Sanal makine için önyükleme tanılama verilerini alır.</span><span class="sxs-lookup"><span data-stu-id="3ed0f-103">Gets boot diagnostics data for a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3ed0f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3ed0f-104">SYNTAX</span></span>

### <span data-ttu-id="3ed0f-105">WindowsParamSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="3ed0f-105">WindowsParamSet (Default)</span></span>
```
Get-AzureRmVMBootDiagnosticsData [-ResourceGroupName] <String> [-Name] <String> [-Windows]
 [-LocalPath] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3ed0f-106">LinuxParamSet</span><span class="sxs-lookup"><span data-stu-id="3ed0f-106">LinuxParamSet</span></span>
```
Get-AzureRmVMBootDiagnosticsData [-ResourceGroupName] <String> [-Name] <String> [-Linux]
 [[-LocalPath] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3ed0f-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="3ed0f-107">DESCRIPTION</span></span>
<span data-ttu-id="3ed0f-108">**Get-AzureRmVMBootDiagnosticsData** cmdlet 'i sanal makine için önyükleme tanılama verilerini alır.</span><span class="sxs-lookup"><span data-stu-id="3ed0f-108">The **Get-AzureRmVMBootDiagnosticsData** cmdlet gets boot diagnostics data for a virtual machine.</span></span>

## <span data-ttu-id="3ed0f-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3ed0f-109">EXAMPLES</span></span>

### <span data-ttu-id="3ed0f-110">Örnek 1: önyükleme tanılama verilerini alma</span><span class="sxs-lookup"><span data-stu-id="3ed0f-110">Example 1: Get boot diagnostics data</span></span>
```
PS C:\> Get-AzureRmVMBootDiagnosticsData -ResourceGroupName "ResourceGroup11" -Name "ContosoVM07" -Windows -LocalPath "C:\Contoso\BootDiagnostics"
```

<span data-ttu-id="3ed0f-111">Bu komut, ContosoVM07 adındaki sanal makine için önyükleme tanılama verilerini alır.</span><span class="sxs-lookup"><span data-stu-id="3ed0f-111">This command gets boot diagnostics data for the virtual machine named ContosoVM07.</span></span>
<span data-ttu-id="3ed0f-112">Bu sanal makine Windows işletim sistemini çalıştırır.</span><span class="sxs-lookup"><span data-stu-id="3ed0f-112">This virtual machine runs the Windows operating system.</span></span>
<span data-ttu-id="3ed0f-113">Komut, verileri belirtilen yerel yolda depolar.</span><span class="sxs-lookup"><span data-stu-id="3ed0f-113">The command stores the data in specified local path.</span></span>

## <span data-ttu-id="3ed0f-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3ed0f-114">PARAMETERS</span></span>

### <span data-ttu-id="3ed0f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ed0f-115">-DefaultProfile</span></span>
<span data-ttu-id="3ed0f-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3ed0f-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3ed0f-117">-Linux</span><span class="sxs-lookup"><span data-stu-id="3ed0f-117">-Linux</span></span>
<span data-ttu-id="3ed0f-118">Sanal makinenin Linux işletim sistemini yürüttüğünde emin olmak.</span><span class="sxs-lookup"><span data-stu-id="3ed0f-118">Indicates that the virtual machine runs the Linux operating system.</span></span>

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

### <span data-ttu-id="3ed0f-119">-LocalPath</span><span class="sxs-lookup"><span data-stu-id="3ed0f-119">-LocalPath</span></span>
<span data-ttu-id="3ed0f-120">Önyükleme Tanılama verileri için yerel yolu belirtir.</span><span class="sxs-lookup"><span data-stu-id="3ed0f-120">Specifies the local path for the boot diagnostics data.</span></span>

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

### <span data-ttu-id="3ed0f-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="3ed0f-121">-Name</span></span>
<span data-ttu-id="3ed0f-122">Bu cmdlet 'in tanılama verilerini aldığı sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3ed0f-122">Specifies the name of the virtual machine for which this cmdlet gets diagnostics data.</span></span>

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

### <span data-ttu-id="3ed0f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ed0f-123">-ResourceGroupName</span></span>
<span data-ttu-id="3ed0f-124">Sanal makinenin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3ed0f-124">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="3ed0f-125">-Windows</span><span class="sxs-lookup"><span data-stu-id="3ed0f-125">-Windows</span></span>
<span data-ttu-id="3ed0f-126">Sanal makinenin Windows işletim sistemini yürüttüi gösterir.</span><span class="sxs-lookup"><span data-stu-id="3ed0f-126">Indicates that the virtual machine runs the Windows operating system.</span></span>

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

### <span data-ttu-id="3ed0f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ed0f-127">CommonParameters</span></span>
<span data-ttu-id="3ed0f-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3ed0f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ed0f-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ed0f-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ed0f-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3ed0f-130">INPUTS</span></span>

## <span data-ttu-id="3ed0f-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3ed0f-131">OUTPUTS</span></span>

## <span data-ttu-id="3ed0f-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3ed0f-132">NOTES</span></span>

## <span data-ttu-id="3ed0f-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3ed0f-133">RELATED LINKS</span></span>

[<span data-ttu-id="3ed0f-134">Set-AzureRmVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="3ed0f-134">Set-AzureRmVMBootDiagnostics</span></span>](./Set-AzureRmVMBootDiagnostics.md)


