---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: D5BEA683-44AE-4D71-827D-02A03F0BEAE9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmdiagnosticsextension
schema: 2.0.0
ms.openlocfilehash: e02c86407326d9ea5b12a5a589e5860c9dfb5c19
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93940196"
---
# <span data-ttu-id="1b1f0-101">Get-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="1b1f0-101">Get-AzureRmVMDiagnosticsExtension</span></span>

## <span data-ttu-id="1b1f0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1b1f0-102">SYNOPSIS</span></span>
<span data-ttu-id="1b1f0-103">Sanal makinedeki tanılama uzantısının ayarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="1b1f0-103">Gets the settings of the Diagnostics extension on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1b1f0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1b1f0-104">SYNTAX</span></span>

```
Get-AzureRmVMDiagnosticsExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1b1f0-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="1b1f0-105">DESCRIPTION</span></span>
<span data-ttu-id="1b1f0-106">**Get-Azurermvmdiagnosticsextenter** cmdlet 'i, bir sanal makinedeki Azure tanılama uzantısının ayarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="1b1f0-106">The **Get-AzureRmVMDiagnosticsExtension** cmdlet gets the settings of the Azure Diagnostics extension on a virtual machine.</span></span>

## <span data-ttu-id="1b1f0-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1b1f0-107">EXAMPLES</span></span>

### <span data-ttu-id="1b1f0-108">Örnek 1: sanal makineye tanılama uzantısı uygulanır</span><span class="sxs-lookup"><span data-stu-id="1b1f0-108">Example 1: Get the diagnostics extension applied to a virtual machine</span></span>
```
PS C:\> Get-AzureRmVMDiagnosticsExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22"
```

<span data-ttu-id="1b1f0-109">Bu komut, ContosoVM22 adındaki sanal makineye uygulanan tanılama uzantısını alır.</span><span class="sxs-lookup"><span data-stu-id="1b1f0-109">This command gets the diagnostics extension applied to the virtual machine named ContosoVM22.</span></span>

## <span data-ttu-id="1b1f0-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1b1f0-110">PARAMETERS</span></span>

### <span data-ttu-id="1b1f0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b1f0-111">-DefaultProfile</span></span>
<span data-ttu-id="1b1f0-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1b1f0-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1b1f0-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="1b1f0-113">-Name</span></span>
<span data-ttu-id="1b1f0-114">Bu cmdlet 'in ayarları aldığı tanılama uzantısının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1b1f0-114">Specifies the name of the Diagnostics extension for which this cmdlet gets settings.</span></span>

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

### <span data-ttu-id="1b1f0-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b1f0-115">-ResourceGroupName</span></span>
<span data-ttu-id="1b1f0-116">Sanal makinenin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1b1f0-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="1b1f0-117">-Durum</span><span class="sxs-lookup"><span data-stu-id="1b1f0-117">-Status</span></span>
<span data-ttu-id="1b1f0-118">Bu cmdlet 'in durum değerini kullandığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1b1f0-118">Indicates that this cmdlet uses the Status value.</span></span>

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

### <span data-ttu-id="1b1f0-119">-VMName</span><span class="sxs-lookup"><span data-stu-id="1b1f0-119">-VMName</span></span>
<span data-ttu-id="1b1f0-120">Bu cmdlet 'in tanılama uzantısını aldığı sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1b1f0-120">Specifies the name of the virtual machine from which this cmdlet gets the Diagnostics extension.</span></span>

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

### <span data-ttu-id="1b1f0-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b1f0-121">CommonParameters</span></span>
<span data-ttu-id="1b1f0-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1b1f0-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b1f0-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b1f0-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b1f0-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1b1f0-124">INPUTS</span></span>

### <span data-ttu-id="1b1f0-125">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="1b1f0-125">None</span></span>
<span data-ttu-id="1b1f0-126">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="1b1f0-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1b1f0-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1b1f0-127">OUTPUTS</span></span>

### <span data-ttu-id="1b1f0-128">Microsoft. Azure. Commands. COMPUTE. modeller. PSVirtualMachineExtension</span><span class="sxs-lookup"><span data-stu-id="1b1f0-128">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtension</span></span>

## <span data-ttu-id="1b1f0-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1b1f0-129">NOTES</span></span>

## <span data-ttu-id="1b1f0-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1b1f0-130">RELATED LINKS</span></span>

[<span data-ttu-id="1b1f0-131">Remove-azurermvmdiagnosticsexten</span><span class="sxs-lookup"><span data-stu-id="1b1f0-131">Remove-AzureRmVMDiagnosticsExtension</span></span>](./Remove-AzureRmVMDiagnosticsExtension.md)

[<span data-ttu-id="1b1f0-132">Set-azurermvmdiagnosticsexten</span><span class="sxs-lookup"><span data-stu-id="1b1f0-132">Set-AzureRmVMDiagnosticsExtension</span></span>](./Set-AzureRMVMDiagnosticsExtension.md)


