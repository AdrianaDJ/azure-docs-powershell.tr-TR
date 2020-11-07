---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 695F224D-DA25-49F2-916E-25DA2A48A4A7
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmdscextensionstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMDscExtensionStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMDscExtensionStatus.md
ms.openlocfilehash: caf6f142c9669ba3f1b5f343c4bbb1a4dc978a97
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752913"
---
# <span data-ttu-id="4389e-101">Get-AzVMDscExtensionStatus</span><span class="sxs-lookup"><span data-stu-id="4389e-101">Get-AzVMDscExtensionStatus</span></span>

## <span data-ttu-id="4389e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4389e-102">SYNOPSIS</span></span>
<span data-ttu-id="4389e-103">Sanal makine için DSC genişletme işleyicisinin durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="4389e-103">Gets the status of the DSC extension handler for a virtual machine.</span></span>

## <span data-ttu-id="4389e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4389e-104">SYNTAX</span></span>

```
Get-AzVMDscExtensionStatus [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4389e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="4389e-105">DESCRIPTION</span></span>
<span data-ttu-id="4389e-106">**Get-AzVMDscExtensionStatus** cmdlet 'i, kaynak grubundaki bir sanal makine Için Istenen durum yapılandırma (DSC) uzantı işleyicisinin durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="4389e-106">The **Get-AzVMDscExtensionStatus** cmdlet gets the status of the Desired State Configuration (DSC) extension handler for a virtual machine in a resource group.</span></span>
<span data-ttu-id="4389e-107">Yapılandırma uygulandığında bu cmdlet Start-DscConfiguration cmdlet ile tutarlı bir çıkış oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4389e-107">When a configuration is applied this cmdlet produces output consistent with the Start-DscConfiguration cmdlet.</span></span>

## <span data-ttu-id="4389e-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4389e-108">EXAMPLES</span></span>

## <span data-ttu-id="4389e-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4389e-109">PARAMETERS</span></span>

### <span data-ttu-id="4389e-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4389e-110">-DefaultProfile</span></span>
<span data-ttu-id="4389e-111">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4389e-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4389e-112">-Ad</span><span class="sxs-lookup"><span data-stu-id="4389e-112">-Name</span></span>
<span data-ttu-id="4389e-113">Uzantıyı temsil eden Azure Resource Manager kaynağının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4389e-113">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="4389e-114">Set-AzVMDscExtension cmdlet 'i **Get-AzVMDscExtensionStatus** tarafından kullanılan aynı değer olan Microsoft. POWERSHELL. DSC olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="4389e-114">The Set-AzVMDscExtension cmdlet sets this name to Microsoft.Powershell.DSC, which is the same value that is used by **Get-AzVMDscExtensionStatus**.</span></span>
<span data-ttu-id="4389e-115">Bu parametreyi yalnızca Set cmdlet 'inde varsayılan adı değiştirdiyseniz veya Kaynak Yöneticisi şablonunda farklı bir kaynak adı kullandıysanız belirtin.</span><span class="sxs-lookup"><span data-stu-id="4389e-115">Specify this parameter only if you changed the default name in the Set cmdlet or used a different resource name in a Resource Manager template.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4389e-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4389e-116">-ResourceGroupName</span></span>
<span data-ttu-id="4389e-117">Sanal makinenin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4389e-117">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="4389e-118">-VMName</span><span class="sxs-lookup"><span data-stu-id="4389e-118">-VMName</span></span>
<span data-ttu-id="4389e-119">Bu cmdlet 'in DSC Uzantısı durumunu aldığı sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4389e-119">Specifies the name of a virtual machine for which this cmdlet gets the DSC extension status.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4389e-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4389e-120">CommonParameters</span></span>
<span data-ttu-id="4389e-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4389e-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4389e-122">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="4389e-122">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4389e-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4389e-123">INPUTS</span></span>

### <span data-ttu-id="4389e-124">System. String</span><span class="sxs-lookup"><span data-stu-id="4389e-124">System.String</span></span>

## <span data-ttu-id="4389e-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4389e-125">OUTPUTS</span></span>

### <span data-ttu-id="4389e-126">Microsoft. Azure. Commands. COMPUTE. modeller. Psvirtualmachineınstanceview</span><span class="sxs-lookup"><span data-stu-id="4389e-126">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineInstanceView</span></span>

## <span data-ttu-id="4389e-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4389e-127">NOTES</span></span>

## <span data-ttu-id="4389e-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4389e-128">RELATED LINKS</span></span>

[<span data-ttu-id="4389e-129">Set-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="4389e-129">Set-AzVMDscExtension</span></span>](./Set-AzVMDscExtension.md)


