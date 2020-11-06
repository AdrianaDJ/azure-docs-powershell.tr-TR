---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 5B7A1BE6-F5F5-4968-BE32-7743D0E25FE3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMDscExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMDscExtension.md
ms.openlocfilehash: 0a3c54331b557b6be279ab5ce3f9fafad62b158c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587634"
---
# <span data-ttu-id="d2386-101">Get-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="d2386-101">Get-AzureRmVMDscExtension</span></span>

## <span data-ttu-id="d2386-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d2386-102">SYNOPSIS</span></span>
<span data-ttu-id="d2386-103">Belirli bir sanal makinedeki DSC uzantısının ayarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="d2386-103">Gets the settings of the DSC extension on a particular virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d2386-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d2386-104">SYNTAX</span></span>

```
Get-AzureRmVMDscExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [<CommonParameters>]
```

## <span data-ttu-id="d2386-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d2386-105">DESCRIPTION</span></span>
<span data-ttu-id="d2386-106">**Get-AzureRmVMDscExtension** cmdlet 'i, belirli bir sanal makinede Istenen durum YAPıLANDıRMASı (DSC) uzantısının ayarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="d2386-106">The **Get-AzureRmVMDscExtension** cmdlet gets the settings of the Desired State Configuration (DSC) extension on a particular virtual machine.</span></span>

## <span data-ttu-id="d2386-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d2386-107">EXAMPLES</span></span>

### <span data-ttu-id="d2386-108">Örnek 1: DSC uzantısının ayarlarını alma</span><span class="sxs-lookup"><span data-stu-id="d2386-108">Example 1: Get the settings of a DSC extension</span></span>
```
PS C:\> Get-AzureRmVMDscExtension -ResourceGroupName "ResourceGroup002" -VMName "VM07" -Name "DSC"
```

<span data-ttu-id="d2386-109">Bu komut, VM07 adındaki sanal makinede DSC adlı uzantının ayarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="d2386-109">This command gets the settings of extension named DSC on the virtual machine named VM07.</span></span>

## <span data-ttu-id="d2386-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d2386-110">PARAMETERS</span></span>

### <span data-ttu-id="d2386-111">-Ad</span><span class="sxs-lookup"><span data-stu-id="d2386-111">-Name</span></span>
<span data-ttu-id="d2386-112">Uzantıyı temsil eden Azure Resource Manager kaynağının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d2386-112">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="d2386-113">Set-AzureRmVMDscExtension cmdlet, **Get-AzureRmVMDscExtension** tarafından kullanılan değer olan Microsoft. POWERSHELL. DSC olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="d2386-113">The Set-AzureRmVMDscExtension cmdlet sets this name to Microsoft.Powershell.DSC, which is the same value that is used by **Get-AzureRmVMDscExtension**.</span></span>
<span data-ttu-id="d2386-114">Bu parametreyi yalnızca **set-AzureRmVMDscExtension** cmdlet 'inde varsayılan adı değiştirdiyseniz veya Kaynak Yöneticisi şablonunda farklı bir kaynak adı kullandıysanız belirtin.</span><span class="sxs-lookup"><span data-stu-id="d2386-114">Specify this parameter only if you changed the default name in the **Set-AzureRmVMDscExtension** cmdlet or used a different resource name in a Resource Manager template.</span></span>

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

### <span data-ttu-id="d2386-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2386-115">-ResourceGroupName</span></span>
<span data-ttu-id="d2386-116">Sanal makinenin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d2386-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="d2386-117">-Durum</span><span class="sxs-lookup"><span data-stu-id="d2386-117">-Status</span></span>
<span data-ttu-id="d2386-118">Bu cmdlet 'in DSC uzantısının örnek görünümünü aldığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d2386-118">Indicates that this cmdlet gets the instance view of the DSC extension.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2386-119">-VMName</span><span class="sxs-lookup"><span data-stu-id="d2386-119">-VMName</span></span>
<span data-ttu-id="d2386-120">Bu cmdlet 'in DSC uzantısını aldığı sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d2386-120">Specifies the name of a virtual machine for which this cmdlet gets the DSC extension.</span></span>

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

### <span data-ttu-id="d2386-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2386-121">CommonParameters</span></span>
<span data-ttu-id="d2386-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d2386-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2386-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2386-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2386-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d2386-124">INPUTS</span></span>

### <span data-ttu-id="d2386-125">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="d2386-125">None</span></span>
<span data-ttu-id="d2386-126">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="d2386-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d2386-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d2386-127">OUTPUTS</span></span>

### <span data-ttu-id="d2386-128">Microsoft. Azure. Commands. COMPUTE. Extension. DSC. VirtualMachineDscExtensionContext</span><span class="sxs-lookup"><span data-stu-id="d2386-128">Microsoft.Azure.Commands.Compute.Extension.DSC.VirtualMachineDscExtensionContext</span></span>

## <span data-ttu-id="d2386-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d2386-129">NOTES</span></span>

## <span data-ttu-id="d2386-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d2386-130">RELATED LINKS</span></span>

[<span data-ttu-id="d2386-131">Remove-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="d2386-131">Remove-AzureRmVMDscExtension</span></span>](./Remove-AzureRmVMDscExtension.md)

[<span data-ttu-id="d2386-132">Set-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="d2386-132">Set-AzureRmVMDscExtension</span></span>](./Set-AzureRmVMDscExtension.md)


