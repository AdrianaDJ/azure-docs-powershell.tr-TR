---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 5B7A1BE6-F5F5-4968-BE32-7743D0E25FE3
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmdscextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMDscExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMDscExtension.md
ms.openlocfilehash: 70f06718c2d96e11b46842e4f39af26d3e29c2f9
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93937024"
---
# <span data-ttu-id="4f503-101">Get-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="4f503-101">Get-AzVMDscExtension</span></span>

## <span data-ttu-id="4f503-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4f503-102">SYNOPSIS</span></span>
<span data-ttu-id="4f503-103">Belirli bir sanal makinedeki DSC uzantısının ayarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="4f503-103">Gets the settings of the DSC extension on a particular virtual machine.</span></span>

## <span data-ttu-id="4f503-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4f503-104">SYNTAX</span></span>

```
Get-AzVMDscExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4f503-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="4f503-105">DESCRIPTION</span></span>
<span data-ttu-id="4f503-106">**Get-AzVMDscExtension** cmdlet 'i, belirli bir sanal makinede Istenen durum YAPıLANDıRMASı (DSC) uzantısının ayarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="4f503-106">The **Get-AzVMDscExtension** cmdlet gets the settings of the Desired State Configuration (DSC) extension on a particular virtual machine.</span></span>

## <span data-ttu-id="4f503-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4f503-107">EXAMPLES</span></span>

### <span data-ttu-id="4f503-108">Örnek 1: DSC uzantısının ayarlarını alma</span><span class="sxs-lookup"><span data-stu-id="4f503-108">Example 1: Get the settings of a DSC extension</span></span>
```
PS C:\> Get-AzVMDscExtension -ResourceGroupName "ResourceGroup002" -VMName "VM07" -Name "DSC"
```

<span data-ttu-id="4f503-109">Bu komut, VM07 adındaki sanal makinede DSC adlı uzantının ayarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="4f503-109">This command gets the settings of extension named DSC on the virtual machine named VM07.</span></span>

## <span data-ttu-id="4f503-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4f503-110">PARAMETERS</span></span>

### <span data-ttu-id="4f503-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f503-111">-DefaultProfile</span></span>
<span data-ttu-id="4f503-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4f503-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4f503-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="4f503-113">-Name</span></span>
<span data-ttu-id="4f503-114">Uzantıyı temsil eden Azure Resource Manager kaynağının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4f503-114">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="4f503-115">Set-AzVMDscExtension cmdlet 'i **Get-AzVMDscExtension** tarafından kullanılan aynı değer olan Microsoft. POWERSHELL. DSC olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="4f503-115">The Set-AzVMDscExtension cmdlet sets this name to Microsoft.Powershell.DSC, which is the same value that is used by **Get-AzVMDscExtension**.</span></span>
<span data-ttu-id="4f503-116">Bu parametreyi yalnızca **set-AzVMDscExtension** cmdlet 'inde varsayılan adı değiştirdiyseniz veya Kaynak Yöneticisi şablonunda farklı bir kaynak adı kullandıysanız belirtin.</span><span class="sxs-lookup"><span data-stu-id="4f503-116">Specify this parameter only if you changed the default name in the **Set-AzVMDscExtension** cmdlet or used a different resource name in a Resource Manager template.</span></span>

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

### <span data-ttu-id="4f503-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f503-117">-ResourceGroupName</span></span>
<span data-ttu-id="4f503-118">Sanal makinenin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4f503-118">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="4f503-119">-Durum</span><span class="sxs-lookup"><span data-stu-id="4f503-119">-Status</span></span>
<span data-ttu-id="4f503-120">Bu cmdlet 'in DSC uzantısının örnek görünümünü aldığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4f503-120">Indicates that this cmdlet gets the instance view of the DSC extension.</span></span>

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

### <span data-ttu-id="4f503-121">-VMName</span><span class="sxs-lookup"><span data-stu-id="4f503-121">-VMName</span></span>
<span data-ttu-id="4f503-122">Bu cmdlet 'in DSC uzantısını aldığı sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4f503-122">Specifies the name of a virtual machine for which this cmdlet gets the DSC extension.</span></span>

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

### <span data-ttu-id="4f503-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f503-123">CommonParameters</span></span>
<span data-ttu-id="4f503-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4f503-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f503-125">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4f503-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f503-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4f503-126">INPUTS</span></span>

### <span data-ttu-id="4f503-127">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="4f503-127">None</span></span>
<span data-ttu-id="4f503-128">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="4f503-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4f503-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4f503-129">OUTPUTS</span></span>

### <span data-ttu-id="4f503-130">Microsoft. Azure. Commands. COMPUTE. Extension. DSC. VirtualMachineDscExtensionContext</span><span class="sxs-lookup"><span data-stu-id="4f503-130">Microsoft.Azure.Commands.Compute.Extension.DSC.VirtualMachineDscExtensionContext</span></span>

## <span data-ttu-id="4f503-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4f503-131">NOTES</span></span>

## <span data-ttu-id="4f503-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4f503-132">RELATED LINKS</span></span>

[<span data-ttu-id="4f503-133">Remove-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="4f503-133">Remove-AzVMDscExtension</span></span>](./Remove-AzVMDscExtension.md)

[<span data-ttu-id="4f503-134">Set-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="4f503-134">Set-AzVMDscExtension</span></span>](./Set-AzVMDscExtension.md)


