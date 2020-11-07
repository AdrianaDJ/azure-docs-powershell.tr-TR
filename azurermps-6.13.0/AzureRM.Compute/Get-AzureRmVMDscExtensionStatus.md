---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 695F224D-DA25-49F2-916E-25DA2A48A4A7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmdscextensionstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMDscExtensionStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMDscExtensionStatus.md
ms.openlocfilehash: 482d2d5b7dd88618bb29270f6ef3cec4e133e842
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763458"
---
# <span data-ttu-id="485e0-101">Get-AzureRmVMDscExtensionStatus</span><span class="sxs-lookup"><span data-stu-id="485e0-101">Get-AzureRmVMDscExtensionStatus</span></span>

## <span data-ttu-id="485e0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="485e0-102">SYNOPSIS</span></span>
<span data-ttu-id="485e0-103">Sanal makine için DSC genişletme işleyicisinin durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="485e0-103">Gets the status of the DSC extension handler for a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="485e0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="485e0-104">SYNTAX</span></span>

```
Get-AzureRmVMDscExtensionStatus [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="485e0-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="485e0-105">DESCRIPTION</span></span>
<span data-ttu-id="485e0-106">**Get-AzureRmVMDscExtensionStatus** cmdlet 'i, kaynak grubundaki sanal makine Için Istenen durum yapılandırma (DSC) uzantı işleyicisinin durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="485e0-106">The **Get-AzureRmVMDscExtensionStatus** cmdlet gets the status of the Desired State Configuration (DSC) extension handler for a virtual machine in a resource group.</span></span>
<span data-ttu-id="485e0-107">Yapılandırma uygulandığında bu cmdlet Start-DscConfiguration cmdlet ile tutarlı bir çıkış oluşturur.</span><span class="sxs-lookup"><span data-stu-id="485e0-107">When a configuration is applied this cmdlet produces output consistent with the Start-DscConfiguration cmdlet.</span></span>

## <span data-ttu-id="485e0-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="485e0-108">EXAMPLES</span></span>

## <span data-ttu-id="485e0-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="485e0-109">PARAMETERS</span></span>

### <span data-ttu-id="485e0-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="485e0-110">-DefaultProfile</span></span>
<span data-ttu-id="485e0-111">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="485e0-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="485e0-112">-Ad</span><span class="sxs-lookup"><span data-stu-id="485e0-112">-Name</span></span>
<span data-ttu-id="485e0-113">Uzantıyı temsil eden Azure Resource Manager kaynağının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="485e0-113">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="485e0-114">Set-AzureRmVMDscExtension cmdlet, **Get-AzureRmVMDscExtensionStatus** tarafından kullanılan aynı değer olan Microsoft. POWERSHELL. DSC olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="485e0-114">The Set-AzureRmVMDscExtension cmdlet sets this name to Microsoft.Powershell.DSC, which is the same value that is used by **Get-AzureRmVMDscExtensionStatus**.</span></span>
<span data-ttu-id="485e0-115">Bu parametreyi yalnızca Set cmdlet 'inde varsayılan adı değiştirdiyseniz veya Kaynak Yöneticisi şablonunda farklı bir kaynak adı kullandıysanız belirtin.</span><span class="sxs-lookup"><span data-stu-id="485e0-115">Specify this parameter only if you changed the default name in the Set cmdlet or used a different resource name in a Resource Manager template.</span></span>

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

### <span data-ttu-id="485e0-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="485e0-116">-ResourceGroupName</span></span>
<span data-ttu-id="485e0-117">Sanal makinenin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="485e0-117">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="485e0-118">-VMName</span><span class="sxs-lookup"><span data-stu-id="485e0-118">-VMName</span></span>
<span data-ttu-id="485e0-119">Bu cmdlet 'in DSC Uzantısı durumunu aldığı sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="485e0-119">Specifies the name of a virtual machine for which this cmdlet gets the DSC extension status.</span></span>

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

### <span data-ttu-id="485e0-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="485e0-120">CommonParameters</span></span>
<span data-ttu-id="485e0-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="485e0-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="485e0-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="485e0-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="485e0-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="485e0-123">INPUTS</span></span>

### <span data-ttu-id="485e0-124">System. String</span><span class="sxs-lookup"><span data-stu-id="485e0-124">System.String</span></span>

## <span data-ttu-id="485e0-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="485e0-125">OUTPUTS</span></span>

### <span data-ttu-id="485e0-126">Microsoft. Azure. Commands. COMPUTE. modeller. Psvirtualmachineınstanceview</span><span class="sxs-lookup"><span data-stu-id="485e0-126">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineInstanceView</span></span>

## <span data-ttu-id="485e0-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="485e0-127">NOTES</span></span>

## <span data-ttu-id="485e0-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="485e0-128">RELATED LINKS</span></span>

[<span data-ttu-id="485e0-129">Set-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="485e0-129">Set-AzureRmVMDscExtension</span></span>](./Set-AzureRmVMDscExtension.md)


