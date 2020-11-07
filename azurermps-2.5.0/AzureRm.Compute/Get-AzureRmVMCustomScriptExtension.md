---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 1017A74D-6420-4E51-A4A4-1AD3AD6D8122
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmcustomscriptextension
schema: 2.0.0
ms.openlocfilehash: b6ce3afb8b280b9ca07746979f0bb5ba425afd82
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93940192"
---
# <span data-ttu-id="47097-101">Get-AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="47097-101">Get-AzureRmVMCustomScriptExtension</span></span>

## <span data-ttu-id="47097-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="47097-102">SYNOPSIS</span></span>
<span data-ttu-id="47097-103">Özel bir komut dosyası uzantısı hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="47097-103">Gets information about a custom script extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="47097-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="47097-104">SYNTAX</span></span>

```
Get-AzureRmVMCustomScriptExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="47097-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="47097-105">DESCRIPTION</span></span>
<span data-ttu-id="47097-106">**Get-AzureRmVMCustomScriptExtension** cmdlet 'i, bir sanal makinedeki özel betik sanal makine uzantısı hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="47097-106">The **Get-AzureRmVMCustomScriptExtension** cmdlet gets information about a custom script Virtual Machine Extension on a virtual machine.</span></span>

## <span data-ttu-id="47097-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="47097-107">EXAMPLES</span></span>

### <span data-ttu-id="47097-108">Örnek 1: özel bir komut dosyası uzantısı alma</span><span class="sxs-lookup"><span data-stu-id="47097-108">Example 1: Get a custom script extension</span></span>
```
PS C:\> $VMCustomScriptExtension = Get-AzureRmVMCustomScriptExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoCustomScript"
```

<span data-ttu-id="47097-109">Bu komut, VirtualMachine07 adındaki sanal makine için ContosoCustomScript adındaki özel komut dosyası uzantısını alır.</span><span class="sxs-lookup"><span data-stu-id="47097-109">This command gets the custom script extension named ContosoCustomScript for the virtual machine named VirtualMachine07.</span></span>

### <span data-ttu-id="47097-110">Örnek 2: özel bir komut dosyası uzantısının örnek görünümünü alma</span><span class="sxs-lookup"><span data-stu-id="47097-110">Example 2: Get the instance view of a custom script extension</span></span>
```
PS C:\> $VMCustomScriptExtension = Get-AzureRmVMCustomScriptExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoCustomScript" -Status
```

<span data-ttu-id="47097-111">Bu komut, VirtualMachine07 adındaki sanal makine için ContosoCustomScript adındaki özel komut dosyası uzantısının örnek görünümünü alır.</span><span class="sxs-lookup"><span data-stu-id="47097-111">This command gets the instance view of the custom script extension named ContosoCustomScript for the virtual machine named VirtualMachine07.</span></span>

## <span data-ttu-id="47097-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="47097-112">PARAMETERS</span></span>

### <span data-ttu-id="47097-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47097-113">-DefaultProfile</span></span>
<span data-ttu-id="47097-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="47097-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="47097-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="47097-115">-Name</span></span>
<span data-ttu-id="47097-116">Bu cmdlet 'in bilgi aldığı özel komut dosyası uzantısının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="47097-116">Specifies the name of the custom script extension about which this cmdlet gets information.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47097-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47097-117">-ResourceGroupName</span></span>
<span data-ttu-id="47097-118">Sanal makinenin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="47097-118">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="47097-119">-Durum</span><span class="sxs-lookup"><span data-stu-id="47097-119">-Status</span></span>
<span data-ttu-id="47097-120">Bu cmdlet 'in özel betik uzantısının örnek görünümünü aldığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="47097-120">Indicates that this cmdlet gets the instance view of the custom script extension.</span></span>

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

### <span data-ttu-id="47097-121">-VMName</span><span class="sxs-lookup"><span data-stu-id="47097-121">-VMName</span></span>
<span data-ttu-id="47097-122">Bu cmdlet 'in özel komut dosyası uzantısını aldığı sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="47097-122">Specifies the name of a virtual machine for which this cmdlet gets the custom script extension.</span></span>

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

### <span data-ttu-id="47097-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47097-123">CommonParameters</span></span>
<span data-ttu-id="47097-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="47097-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47097-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="47097-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47097-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="47097-126">INPUTS</span></span>

### <span data-ttu-id="47097-127">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="47097-127">None</span></span>
<span data-ttu-id="47097-128">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="47097-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="47097-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="47097-129">OUTPUTS</span></span>

### <span data-ttu-id="47097-130">Microsoft. Azure. Commands. COMPUTE. model. Virtualmachineccustomscriplersioncontext</span><span class="sxs-lookup"><span data-stu-id="47097-130">Microsoft.Azure.Commands.Compute.Models.VirtualMachineCustomScriptExtensionContext</span></span>

## <span data-ttu-id="47097-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="47097-131">NOTES</span></span>

## <span data-ttu-id="47097-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="47097-132">RELATED LINKS</span></span>

[<span data-ttu-id="47097-133">Get-Azurermvmaccessextenma</span><span class="sxs-lookup"><span data-stu-id="47097-133">Get-AzureRmVMAccessExtension</span></span>](./Get-AzureRmVMAccessExtension.md)

[<span data-ttu-id="47097-134">Get-Azurermvmexgeri</span><span class="sxs-lookup"><span data-stu-id="47097-134">Get-AzureRmVMExtension</span></span>](./Get-AzureRmVMExtension.md)

[<span data-ttu-id="47097-135">Get-Azurermvmextensionımage</span><span class="sxs-lookup"><span data-stu-id="47097-135">Get-AzureRmVMExtensionImage</span></span>](./Get-AzureRmVMExtensionImage.md)


