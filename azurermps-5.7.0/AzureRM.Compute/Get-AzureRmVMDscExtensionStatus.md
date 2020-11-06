---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 695F224D-DA25-49F2-916E-25DA2A48A4A7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMDscExtensionStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMDscExtensionStatus.md
ms.openlocfilehash: 7cb7f175cc15e7d4e0915b6af9ef6fe6bdfc74d9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587631"
---
# <span data-ttu-id="1a99a-101">Get-AzureRmVMDscExtensionStatus</span><span class="sxs-lookup"><span data-stu-id="1a99a-101">Get-AzureRmVMDscExtensionStatus</span></span>

## <span data-ttu-id="1a99a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1a99a-102">SYNOPSIS</span></span>
<span data-ttu-id="1a99a-103">Sanal makine için DSC genişletme işleyicisinin durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="1a99a-103">Gets the status of the DSC extension handler for a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1a99a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1a99a-104">SYNTAX</span></span>

```
Get-AzureRmVMDscExtensionStatus [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="1a99a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="1a99a-105">DESCRIPTION</span></span>
<span data-ttu-id="1a99a-106">**Get-AzureRmVMDscExtensionStatus** cmdlet 'i, kaynak grubundaki sanal makine Için Istenen durum yapılandırma (DSC) uzantı işleyicisinin durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="1a99a-106">The **Get-AzureRmVMDscExtensionStatus** cmdlet gets the status of the Desired State Configuration (DSC) extension handler for a virtual machine in a resource group.</span></span>
<span data-ttu-id="1a99a-107">Yapılandırma uygulandığında bu cmdlet Start-DscConfiguration cmdlet ile tutarlı bir çıkış oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1a99a-107">When a configuration is applied this cmdlet produces output consistent with the Start-DscConfiguration cmdlet.</span></span>

## <span data-ttu-id="1a99a-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1a99a-108">EXAMPLES</span></span>

## <span data-ttu-id="1a99a-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1a99a-109">PARAMETERS</span></span>

### <span data-ttu-id="1a99a-110">-Ad</span><span class="sxs-lookup"><span data-stu-id="1a99a-110">-Name</span></span>
<span data-ttu-id="1a99a-111">Uzantıyı temsil eden Azure Resource Manager kaynağının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1a99a-111">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="1a99a-112">Set-AzureRmVMDscExtension cmdlet, **Get-AzureRmVMDscExtensionStatus** tarafından kullanılan aynı değer olan Microsoft. POWERSHELL. DSC olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="1a99a-112">The Set-AzureRmVMDscExtension cmdlet sets this name to Microsoft.Powershell.DSC, which is the same value that is used by **Get-AzureRmVMDscExtensionStatus**.</span></span>
<span data-ttu-id="1a99a-113">Bu parametreyi yalnızca Set cmdlet 'inde varsayılan adı değiştirdiyseniz veya Kaynak Yöneticisi şablonunda farklı bir kaynak adı kullandıysanız belirtin.</span><span class="sxs-lookup"><span data-stu-id="1a99a-113">Specify this parameter only if you changed the default name in the Set cmdlet or used a different resource name in a Resource Manager template.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a99a-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a99a-114">-ResourceGroupName</span></span>
<span data-ttu-id="1a99a-115">Sanal makinenin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1a99a-115">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="1a99a-116">-VMName</span><span class="sxs-lookup"><span data-stu-id="1a99a-116">-VMName</span></span>
<span data-ttu-id="1a99a-117">Bu cmdlet 'in DSC Uzantısı durumunu aldığı sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1a99a-117">Specifies the name of a virtual machine for which this cmdlet gets the DSC extension status.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a99a-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a99a-118">CommonParameters</span></span>
<span data-ttu-id="1a99a-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1a99a-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a99a-120">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a99a-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a99a-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1a99a-121">INPUTS</span></span>

### <span data-ttu-id="1a99a-122">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="1a99a-122">None</span></span>
<span data-ttu-id="1a99a-123">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="1a99a-123">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1a99a-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1a99a-124">OUTPUTS</span></span>

## <span data-ttu-id="1a99a-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1a99a-125">NOTES</span></span>

## <span data-ttu-id="1a99a-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1a99a-126">RELATED LINKS</span></span>

[<span data-ttu-id="1a99a-127">Set-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="1a99a-127">Set-AzureRmVMDscExtension</span></span>](./Set-AzureRmVMDscExtension.md)


