---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D5BEA683-44AE-4D71-827D-02A03F0BEAE9
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmdiagnosticsextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMDiagnosticsExtension.md
ms.openlocfilehash: 6b857356ea35476117a58f8f31f7174a7a91767a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93761349"
---
# <span data-ttu-id="3ac99-101">Get-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="3ac99-101">Get-AzVMDiagnosticsExtension</span></span>

## <span data-ttu-id="3ac99-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3ac99-102">SYNOPSIS</span></span>
<span data-ttu-id="3ac99-103">Sanal makinedeki tanılama uzantısının ayarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="3ac99-103">Gets the settings of the Diagnostics extension on a virtual machine.</span></span>

## <span data-ttu-id="3ac99-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3ac99-104">SYNTAX</span></span>

```
Get-AzVMDiagnosticsExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3ac99-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="3ac99-105">DESCRIPTION</span></span>
<span data-ttu-id="3ac99-106">**Get-Azvmdiagnosticsextenma** cmdlet 'ı, Azure Diagnostics uzantısının sanal makinede ayarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="3ac99-106">The **Get-AzVMDiagnosticsExtension** cmdlet gets the settings of the Azure Diagnostics extension on a virtual machine.</span></span>

## <span data-ttu-id="3ac99-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3ac99-107">EXAMPLES</span></span>

### <span data-ttu-id="3ac99-108">Örnek 1: sanal makineye tanılama uzantısı uygulanır</span><span class="sxs-lookup"><span data-stu-id="3ac99-108">Example 1: Get the diagnostics extension applied to a virtual machine</span></span>
```
PS C:\> Get-AzVMDiagnosticsExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22"
```

<span data-ttu-id="3ac99-109">Bu komut, ContosoVM22 adındaki sanal makineye uygulanan tanılama uzantısını alır.</span><span class="sxs-lookup"><span data-stu-id="3ac99-109">This command gets the diagnostics extension applied to the virtual machine named ContosoVM22.</span></span>

## <span data-ttu-id="3ac99-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3ac99-110">PARAMETERS</span></span>

### <span data-ttu-id="3ac99-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ac99-111">-DefaultProfile</span></span>
<span data-ttu-id="3ac99-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3ac99-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3ac99-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="3ac99-113">-Name</span></span>
<span data-ttu-id="3ac99-114">Bu cmdlet 'in ayarları aldığı tanılama uzantısının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3ac99-114">Specifies the name of the Diagnostics extension for which this cmdlet gets settings.</span></span>

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

### <span data-ttu-id="3ac99-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ac99-115">-ResourceGroupName</span></span>
<span data-ttu-id="3ac99-116">Sanal makinenin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3ac99-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="3ac99-117">-Durum</span><span class="sxs-lookup"><span data-stu-id="3ac99-117">-Status</span></span>
<span data-ttu-id="3ac99-118">Bu cmdlet 'in durum değerini kullandığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3ac99-118">Indicates that this cmdlet uses the Status value.</span></span>

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

### <span data-ttu-id="3ac99-119">-VMName</span><span class="sxs-lookup"><span data-stu-id="3ac99-119">-VMName</span></span>
<span data-ttu-id="3ac99-120">Bu cmdlet 'in tanılama uzantısını aldığı sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3ac99-120">Specifies the name of the virtual machine from which this cmdlet gets the Diagnostics extension.</span></span>

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

### <span data-ttu-id="3ac99-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ac99-121">CommonParameters</span></span>
<span data-ttu-id="3ac99-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3ac99-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ac99-123">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="3ac99-123">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ac99-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3ac99-124">INPUTS</span></span>

### <span data-ttu-id="3ac99-125">System. String</span><span class="sxs-lookup"><span data-stu-id="3ac99-125">System.String</span></span>

### <span data-ttu-id="3ac99-126">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="3ac99-126">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="3ac99-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3ac99-127">OUTPUTS</span></span>

### <span data-ttu-id="3ac99-128">Microsoft. Azure. Commands. COMPUTE. modeller. PSVirtualMachineExtension</span><span class="sxs-lookup"><span data-stu-id="3ac99-128">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtension</span></span>

## <span data-ttu-id="3ac99-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3ac99-129">NOTES</span></span>

## <span data-ttu-id="3ac99-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3ac99-130">RELATED LINKS</span></span>

[<span data-ttu-id="3ac99-131">Remove-azvmdiagnosticsexten</span><span class="sxs-lookup"><span data-stu-id="3ac99-131">Remove-AzVMDiagnosticsExtension</span></span>](./Remove-AzVMDiagnosticsExtension.md)

[<span data-ttu-id="3ac99-132">Set-azvmdiagnosticsexten</span><span class="sxs-lookup"><span data-stu-id="3ac99-132">Set-AzVMDiagnosticsExtension</span></span>](./Set-AzVMDiagnosticsExtension.md)


