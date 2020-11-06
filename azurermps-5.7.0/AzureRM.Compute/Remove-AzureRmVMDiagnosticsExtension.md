---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 89DA3965-5344-4A1D-AEF1-10EA58E129CF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMDiagnosticsExtension.md
ms.openlocfilehash: b9c2499c3172fcd34000c8adaa0bde144217bcbf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589851"
---
# <span data-ttu-id="68849-101">Remove-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="68849-101">Remove-AzureRmVMDiagnosticsExtension</span></span>

## <span data-ttu-id="68849-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="68849-102">SYNOPSIS</span></span>
<span data-ttu-id="68849-103">Sanal makineden tanılama uzantısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="68849-103">Removes the Diagnostics extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="68849-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="68849-104">SYNTAX</span></span>

```
Remove-AzureRmVMDiagnosticsExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="68849-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="68849-105">DESCRIPTION</span></span>
<span data-ttu-id="68849-106">**Remove-Azurermvmdiagnosticsextenma** cmdlet 'i, bir Azure Diagnostics uzantısını sanal makineden kaldırır.</span><span class="sxs-lookup"><span data-stu-id="68849-106">The **Remove-AzureRmVMDiagnosticsExtension** cmdlet removes an Azure Diagnostics extension from a virtual machine.</span></span>
<span data-ttu-id="68849-107">Değişikliklerinizi uygulamak için bu cmdlet 'in çıkışını Update-AzureRmVM cmdlet 'ine geçirmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="68849-107">You must pass the output of this cmdlet to the Update-AzureRmVM cmdlet to implement your changes.</span></span>

## <span data-ttu-id="68849-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="68849-108">EXAMPLES</span></span>

### <span data-ttu-id="68849-109">Örnek 1: sanal makineden tanılama uzantısını kaldırma</span><span class="sxs-lookup"><span data-stu-id="68849-109">Example 1: Remove the Diagnostics extension from a virtual machine</span></span>
```
PS C:\> Remove-AzureRmVMDiagnosticsExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22" | Update-AzureRmVM
```

<span data-ttu-id="68849-110">Bu komut, ContosoVM22 adındaki bir sanal makineden tanılama uzantısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="68849-110">This command removes the Diagnostics extension from a virtual machine named ContosoVM22.</span></span>
<span data-ttu-id="68849-111">Komut sonucu, ardışık düzen işlecini kullanarak Update-AzureRmVM cmdlet 'ine geçirir.</span><span class="sxs-lookup"><span data-stu-id="68849-111">The command passes the result to the Update-AzureRmVM cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="68849-112">Bu komut sanal makineyi güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="68849-112">That command updates the virtual machine.</span></span>

## <span data-ttu-id="68849-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="68849-113">PARAMETERS</span></span>

### <span data-ttu-id="68849-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="68849-114">-Name</span></span>
<span data-ttu-id="68849-115">Bu cmdlet 'in kaldırıldığı tanılama uzantısının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="68849-115">Specifies the name of the Diagnostics extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="68849-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68849-116">-ResourceGroupName</span></span>
<span data-ttu-id="68849-117">Sanal makinenin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="68849-117">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="68849-118">-VMName</span><span class="sxs-lookup"><span data-stu-id="68849-118">-VMName</span></span>
<span data-ttu-id="68849-119">Bu cmdlet 'in tanılama uzantısını kaldırdığı sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="68849-119">Specifies the name of the virtual machine from which this cmdlet removes a Diagnostics extension.</span></span>

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

### <span data-ttu-id="68849-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68849-120">CommonParameters</span></span>
<span data-ttu-id="68849-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="68849-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68849-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="68849-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68849-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="68849-123">INPUTS</span></span>

### <span data-ttu-id="68849-124">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="68849-124">None</span></span>
<span data-ttu-id="68849-125">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="68849-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="68849-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="68849-126">OUTPUTS</span></span>

## <span data-ttu-id="68849-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="68849-127">NOTES</span></span>

## <span data-ttu-id="68849-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="68849-128">RELATED LINKS</span></span>

[<span data-ttu-id="68849-129">Get-azurermvmdiagnosticsexten</span><span class="sxs-lookup"><span data-stu-id="68849-129">Get-AzureRmVMDiagnosticsExtension</span></span>](./Get-AzureRMVMDiagnosticsExtension.md)

[<span data-ttu-id="68849-130">Set-azurermvmdiagnosticsexten</span><span class="sxs-lookup"><span data-stu-id="68849-130">Set-AzureRmVMDiagnosticsExtension</span></span>](./Set-AzureRMVMDiagnosticsExtension.md)

[<span data-ttu-id="68849-131">Güncelleştirme-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="68849-131">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


