---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 695F224D-DA25-49F2-916E-25DA2A48A4A7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmdscextensionstatus
schema: 2.0.0
ms.openlocfilehash: b6ec9918657c191e31e10c04b799603654d39d56
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93938890"
---
# <span data-ttu-id="b38d0-101">Get-AzureRmVMDscExtensionStatus</span><span class="sxs-lookup"><span data-stu-id="b38d0-101">Get-AzureRmVMDscExtensionStatus</span></span>

## <span data-ttu-id="b38d0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b38d0-102">SYNOPSIS</span></span>
<span data-ttu-id="b38d0-103">Sanal makine için DSC genişletme işleyicisinin durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="b38d0-103">Gets the status of the DSC extension handler for a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b38d0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b38d0-104">SYNTAX</span></span>

```
Get-AzureRmVMDscExtensionStatus [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b38d0-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b38d0-105">DESCRIPTION</span></span>
<span data-ttu-id="b38d0-106">**Get-AzureRmVMDscExtensionStatus** cmdlet 'i, kaynak grubundaki sanal makine Için Istenen durum yapılandırma (DSC) uzantı işleyicisinin durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="b38d0-106">The **Get-AzureRmVMDscExtensionStatus** cmdlet gets the status of the Desired State Configuration (DSC) extension handler for a virtual machine in a resource group.</span></span>
<span data-ttu-id="b38d0-107">Yapılandırma uygulandığında bu cmdlet Start-DscConfiguration cmdlet ile tutarlı bir çıkış oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b38d0-107">When a configuration is applied this cmdlet produces output consistent with the Start-DscConfiguration cmdlet.</span></span>

## <span data-ttu-id="b38d0-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b38d0-108">EXAMPLES</span></span>

### <span data-ttu-id="b38d0-109">2</span><span class="sxs-lookup"><span data-stu-id="b38d0-109">1:</span></span>
```

```

## <span data-ttu-id="b38d0-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b38d0-110">PARAMETERS</span></span>

### <span data-ttu-id="b38d0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b38d0-111">-DefaultProfile</span></span>
<span data-ttu-id="b38d0-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b38d0-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b38d0-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="b38d0-113">-Name</span></span>
<span data-ttu-id="b38d0-114">Uzantıyı temsil eden Azure Resource Manager kaynağının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b38d0-114">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="b38d0-115">Set-AzureRmVMDscExtension cmdlet, **Get-AzureRmVMDscExtensionStatus** tarafından kullanılan aynı değer olan Microsoft. POWERSHELL. DSC olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="b38d0-115">The Set-AzureRmVMDscExtension cmdlet sets this name to Microsoft.Powershell.DSC, which is the same value that is used by **Get-AzureRmVMDscExtensionStatus**.</span></span>
<span data-ttu-id="b38d0-116">Bu parametreyi yalnızca Set cmdlet 'inde varsayılan adı değiştirdiyseniz veya Kaynak Yöneticisi şablonunda farklı bir kaynak adı kullandıysanız belirtin.</span><span class="sxs-lookup"><span data-stu-id="b38d0-116">Specify this parameter only if you changed the default name in the Set cmdlet or used a different resource name in a Resource Manager template.</span></span>

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

### <span data-ttu-id="b38d0-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b38d0-117">-ResourceGroupName</span></span>
<span data-ttu-id="b38d0-118">Sanal makinenin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b38d0-118">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="b38d0-119">-VMName</span><span class="sxs-lookup"><span data-stu-id="b38d0-119">-VMName</span></span>
<span data-ttu-id="b38d0-120">Bu cmdlet 'in DSC Uzantısı durumunu aldığı sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b38d0-120">Specifies the name of a virtual machine for which this cmdlet gets the DSC extension status.</span></span>

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

### <span data-ttu-id="b38d0-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b38d0-121">CommonParameters</span></span>
<span data-ttu-id="b38d0-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b38d0-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b38d0-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b38d0-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b38d0-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b38d0-124">INPUTS</span></span>

### <span data-ttu-id="b38d0-125">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="b38d0-125">None</span></span>
<span data-ttu-id="b38d0-126">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="b38d0-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b38d0-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b38d0-127">OUTPUTS</span></span>

### <span data-ttu-id="b38d0-128">Microsoft. Azure. Commands. COMPUTE. modeller. Psvirtualmachineınstanceview</span><span class="sxs-lookup"><span data-stu-id="b38d0-128">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineInstanceView</span></span>

## <span data-ttu-id="b38d0-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b38d0-129">NOTES</span></span>

## <span data-ttu-id="b38d0-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b38d0-130">RELATED LINKS</span></span>

[<span data-ttu-id="b38d0-131">Set-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="b38d0-131">Set-AzureRmVMDscExtension</span></span>](./Set-AzureRmVMDscExtension.md)


