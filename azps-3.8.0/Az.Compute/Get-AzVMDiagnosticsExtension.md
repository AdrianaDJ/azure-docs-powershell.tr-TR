---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D5BEA683-44AE-4D71-827D-02A03F0BEAE9
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmdiagnosticsextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMDiagnosticsExtension.md
ms.openlocfilehash: bd56d9e76ffc71d75de0a29fa40291cb405e57fe
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94105052"
---
# <span data-ttu-id="36378-101">Get-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="36378-101">Get-AzVMDiagnosticsExtension</span></span>

## <span data-ttu-id="36378-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="36378-102">SYNOPSIS</span></span>
<span data-ttu-id="36378-103">Sanal makinedeki tanılama uzantısının ayarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="36378-103">Gets the settings of the Diagnostics extension on a virtual machine.</span></span>

## <span data-ttu-id="36378-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="36378-104">SYNTAX</span></span>

```
Get-AzVMDiagnosticsExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="36378-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="36378-105">DESCRIPTION</span></span>
<span data-ttu-id="36378-106">**Get-Azvmdiagnosticsextenma** cmdlet 'ı, Azure Diagnostics uzantısının sanal makinede ayarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="36378-106">The **Get-AzVMDiagnosticsExtension** cmdlet gets the settings of the Azure Diagnostics extension on a virtual machine.</span></span>

## <span data-ttu-id="36378-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="36378-107">EXAMPLES</span></span>

### <span data-ttu-id="36378-108">Örnek 1: sanal makineye tanılama uzantısı uygulanır</span><span class="sxs-lookup"><span data-stu-id="36378-108">Example 1: Get the diagnostics extension applied to a virtual machine</span></span>
```
PS C:\> Get-AzVMDiagnosticsExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22"
```

<span data-ttu-id="36378-109">Bu komut, ContosoVM22 adındaki sanal makineye uygulanan tanılama uzantısını alır.</span><span class="sxs-lookup"><span data-stu-id="36378-109">This command gets the diagnostics extension applied to the virtual machine named ContosoVM22.</span></span>

## <span data-ttu-id="36378-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="36378-110">PARAMETERS</span></span>

### <span data-ttu-id="36378-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36378-111">-DefaultProfile</span></span>
<span data-ttu-id="36378-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="36378-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36378-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="36378-113">-Name</span></span>
<span data-ttu-id="36378-114">Bu cmdlet 'in ayarları aldığı tanılama uzantısının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="36378-114">Specifies the name of the Diagnostics extension for which this cmdlet gets settings.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36378-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36378-115">-ResourceGroupName</span></span>
<span data-ttu-id="36378-116">Sanal makinenin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="36378-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="36378-117">-Durum</span><span class="sxs-lookup"><span data-stu-id="36378-117">-Status</span></span>
<span data-ttu-id="36378-118">Bu cmdlet 'in durum değerini kullandığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="36378-118">Indicates that this cmdlet uses the Status value.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36378-119">-VMName</span><span class="sxs-lookup"><span data-stu-id="36378-119">-VMName</span></span>
<span data-ttu-id="36378-120">Bu cmdlet 'in tanılama uzantısını aldığı sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="36378-120">Specifies the name of the virtual machine from which this cmdlet gets the Diagnostics extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36378-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36378-121">CommonParameters</span></span>
<span data-ttu-id="36378-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="36378-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36378-123">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="36378-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36378-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="36378-124">INPUTS</span></span>

### <span data-ttu-id="36378-125">System. String</span><span class="sxs-lookup"><span data-stu-id="36378-125">System.String</span></span>

### <span data-ttu-id="36378-126">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="36378-126">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="36378-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="36378-127">OUTPUTS</span></span>

### <span data-ttu-id="36378-128">Microsoft. Azure. Commands. COMPUTE. modeller. PSVirtualMachineExtension</span><span class="sxs-lookup"><span data-stu-id="36378-128">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtension</span></span>

## <span data-ttu-id="36378-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="36378-129">NOTES</span></span>

## <span data-ttu-id="36378-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="36378-130">RELATED LINKS</span></span>

[<span data-ttu-id="36378-131">Remove-azvmdiagnosticsexten</span><span class="sxs-lookup"><span data-stu-id="36378-131">Remove-AzVMDiagnosticsExtension</span></span>](./Remove-AzVMDiagnosticsExtension.md)

[<span data-ttu-id="36378-132">Set-azvmdiagnosticsexten</span><span class="sxs-lookup"><span data-stu-id="36378-132">Set-AzVMDiagnosticsExtension</span></span>](./Set-AzVMDiagnosticsExtension.md)


