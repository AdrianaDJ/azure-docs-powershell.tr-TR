---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: D5BEA683-44AE-4D71-827D-02A03F0BEAE9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRMVMDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRMVMDiagnosticsExtension.md
ms.openlocfilehash: 32d3d5a152f36c0e4e5f8e3e4e4ecc2b8eb6ee31
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590518"
---
# <span data-ttu-id="95a1f-101">Get-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="95a1f-101">Get-AzureRmVMDiagnosticsExtension</span></span>

## <span data-ttu-id="95a1f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="95a1f-102">SYNOPSIS</span></span>
<span data-ttu-id="95a1f-103">Sanal makinedeki tanılama uzantısının ayarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="95a1f-103">Gets the settings of the Diagnostics extension on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="95a1f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="95a1f-104">SYNTAX</span></span>

```
Get-AzureRmVMDiagnosticsExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [<CommonParameters>]
```

## <span data-ttu-id="95a1f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="95a1f-105">DESCRIPTION</span></span>
<span data-ttu-id="95a1f-106">**Get-Azurermvmdiagnosticsextenter** cmdlet 'i, bir sanal makinedeki Azure tanılama uzantısının ayarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="95a1f-106">The **Get-AzureRmVMDiagnosticsExtension** cmdlet gets the settings of the Azure Diagnostics extension on a virtual machine.</span></span>

## <span data-ttu-id="95a1f-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="95a1f-107">EXAMPLES</span></span>

### <span data-ttu-id="95a1f-108">Örnek 1: sanal makineye tanılama uzantısı uygulanır</span><span class="sxs-lookup"><span data-stu-id="95a1f-108">Example 1: Get the diagnostics extension applied to a virtual machine</span></span>
```
PS C:\> Get-AzureRmVMDiagnosticsExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22"
```

<span data-ttu-id="95a1f-109">Bu komut, ContosoVM22 adındaki sanal makineye uygulanan tanılama uzantısını alır.</span><span class="sxs-lookup"><span data-stu-id="95a1f-109">This command gets the diagnostics extension applied to the virtual machine named ContosoVM22.</span></span>

## <span data-ttu-id="95a1f-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="95a1f-110">PARAMETERS</span></span>

### <span data-ttu-id="95a1f-111">-Ad</span><span class="sxs-lookup"><span data-stu-id="95a1f-111">-Name</span></span>
<span data-ttu-id="95a1f-112">Bu cmdlet 'in ayarları aldığı tanılama uzantısının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="95a1f-112">Specifies the name of the Diagnostics extension for which this cmdlet gets settings.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95a1f-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95a1f-113">-ResourceGroupName</span></span>
<span data-ttu-id="95a1f-114">Sanal makinenin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="95a1f-114">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="95a1f-115">-Durum</span><span class="sxs-lookup"><span data-stu-id="95a1f-115">-Status</span></span>
<span data-ttu-id="95a1f-116">Bu cmdlet 'in durum değerini kullandığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="95a1f-116">Indicates that this cmdlet uses the Status value.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95a1f-117">-VMName</span><span class="sxs-lookup"><span data-stu-id="95a1f-117">-VMName</span></span>
<span data-ttu-id="95a1f-118">Bu cmdlet 'in tanılama uzantısını aldığı sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="95a1f-118">Specifies the name of the virtual machine from which this cmdlet gets the Diagnostics extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95a1f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95a1f-119">CommonParameters</span></span>
<span data-ttu-id="95a1f-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="95a1f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95a1f-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95a1f-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95a1f-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="95a1f-122">INPUTS</span></span>

### <span data-ttu-id="95a1f-123">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="95a1f-123">None</span></span>
<span data-ttu-id="95a1f-124">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="95a1f-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="95a1f-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="95a1f-125">OUTPUTS</span></span>

## <span data-ttu-id="95a1f-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="95a1f-126">NOTES</span></span>

## <span data-ttu-id="95a1f-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="95a1f-127">RELATED LINKS</span></span>

[<span data-ttu-id="95a1f-128">Remove-azurermvmdiagnosticsexten</span><span class="sxs-lookup"><span data-stu-id="95a1f-128">Remove-AzureRmVMDiagnosticsExtension</span></span>](./Remove-AzureRmVMDiagnosticsExtension.md)

[<span data-ttu-id="95a1f-129">Set-azurermvmdiagnosticsexten</span><span class="sxs-lookup"><span data-stu-id="95a1f-129">Set-AzureRmVMDiagnosticsExtension</span></span>](./Set-AzureRMVMDiagnosticsExtension.md)


