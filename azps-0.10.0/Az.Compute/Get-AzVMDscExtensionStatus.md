---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 695F224D-DA25-49F2-916E-25DA2A48A4A7
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmdscextensionstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMDscExtensionStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMDscExtensionStatus.md
ms.openlocfilehash: 3ae9827c6db5136b9327936a63ac0441dcf94ff1
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93937020"
---
# <span data-ttu-id="f41fa-101">Get-AzVMDscExtensionStatus</span><span class="sxs-lookup"><span data-stu-id="f41fa-101">Get-AzVMDscExtensionStatus</span></span>

## <span data-ttu-id="f41fa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f41fa-102">SYNOPSIS</span></span>
<span data-ttu-id="f41fa-103">Sanal makine için DSC genişletme işleyicisinin durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="f41fa-103">Gets the status of the DSC extension handler for a virtual machine.</span></span>

## <span data-ttu-id="f41fa-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f41fa-104">SYNTAX</span></span>

```
Get-AzVMDscExtensionStatus [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f41fa-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f41fa-105">DESCRIPTION</span></span>
<span data-ttu-id="f41fa-106">**Get-AzVMDscExtensionStatus** cmdlet 'i, kaynak grubundaki bir sanal makine Için Istenen durum yapılandırma (DSC) uzantı işleyicisinin durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="f41fa-106">The **Get-AzVMDscExtensionStatus** cmdlet gets the status of the Desired State Configuration (DSC) extension handler for a virtual machine in a resource group.</span></span>
<span data-ttu-id="f41fa-107">Yapılandırma uygulandığında bu cmdlet Start-DscConfiguration cmdlet ile tutarlı bir çıkış oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f41fa-107">When a configuration is applied this cmdlet produces output consistent with the Start-DscConfiguration cmdlet.</span></span>

## <span data-ttu-id="f41fa-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f41fa-108">EXAMPLES</span></span>

### <span data-ttu-id="f41fa-109">2</span><span class="sxs-lookup"><span data-stu-id="f41fa-109">1:</span></span>
```

```

## <span data-ttu-id="f41fa-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f41fa-110">PARAMETERS</span></span>

### <span data-ttu-id="f41fa-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f41fa-111">-DefaultProfile</span></span>
<span data-ttu-id="f41fa-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f41fa-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f41fa-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="f41fa-113">-Name</span></span>
<span data-ttu-id="f41fa-114">Uzantıyı temsil eden Azure Resource Manager kaynağının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f41fa-114">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="f41fa-115">Set-AzVMDscExtension cmdlet 'i **Get-AzVMDscExtensionStatus** tarafından kullanılan aynı değer olan Microsoft. POWERSHELL. DSC olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="f41fa-115">The Set-AzVMDscExtension cmdlet sets this name to Microsoft.Powershell.DSC, which is the same value that is used by **Get-AzVMDscExtensionStatus**.</span></span>
<span data-ttu-id="f41fa-116">Bu parametreyi yalnızca Set cmdlet 'inde varsayılan adı değiştirdiyseniz veya Kaynak Yöneticisi şablonunda farklı bir kaynak adı kullandıysanız belirtin.</span><span class="sxs-lookup"><span data-stu-id="f41fa-116">Specify this parameter only if you changed the default name in the Set cmdlet or used a different resource name in a Resource Manager template.</span></span>

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

### <span data-ttu-id="f41fa-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f41fa-117">-ResourceGroupName</span></span>
<span data-ttu-id="f41fa-118">Sanal makinenin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f41fa-118">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="f41fa-119">-VMName</span><span class="sxs-lookup"><span data-stu-id="f41fa-119">-VMName</span></span>
<span data-ttu-id="f41fa-120">Bu cmdlet 'in DSC Uzantısı durumunu aldığı sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f41fa-120">Specifies the name of a virtual machine for which this cmdlet gets the DSC extension status.</span></span>

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

### <span data-ttu-id="f41fa-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f41fa-121">CommonParameters</span></span>
<span data-ttu-id="f41fa-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f41fa-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f41fa-123">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f41fa-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f41fa-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f41fa-124">INPUTS</span></span>

### <span data-ttu-id="f41fa-125">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="f41fa-125">None</span></span>
<span data-ttu-id="f41fa-126">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="f41fa-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f41fa-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f41fa-127">OUTPUTS</span></span>

### <span data-ttu-id="f41fa-128">Microsoft. Azure. Commands. COMPUTE. modeller. Psvirtualmachineınstanceview</span><span class="sxs-lookup"><span data-stu-id="f41fa-128">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineInstanceView</span></span>

## <span data-ttu-id="f41fa-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f41fa-129">NOTES</span></span>

## <span data-ttu-id="f41fa-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f41fa-130">RELATED LINKS</span></span>

[<span data-ttu-id="f41fa-131">Set-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="f41fa-131">Set-AzVMDscExtension</span></span>](./Set-AzVMDscExtension.md)


