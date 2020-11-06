---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 1017A74D-6420-4E51-A4A4-1AD3AD6D8122
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMCustomScriptExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMCustomScriptExtension.md
ms.openlocfilehash: d06e2ca5ed51b89b78999c1e146ca75805c8a674
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592650"
---
# <span data-ttu-id="0d21a-101">Get-AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="0d21a-101">Get-AzureRmVMCustomScriptExtension</span></span>

## <span data-ttu-id="0d21a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0d21a-102">SYNOPSIS</span></span>
<span data-ttu-id="0d21a-103">Özel bir komut dosyası uzantısı hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="0d21a-103">Gets information about a custom script extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0d21a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0d21a-104">SYNTAX</span></span>

```
Get-AzureRmVMCustomScriptExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0d21a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="0d21a-105">DESCRIPTION</span></span>
<span data-ttu-id="0d21a-106">**Get-AzureRmVMCustomScriptExtension** cmdlet 'i, bir sanal makinedeki özel betik sanal makine uzantısı hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="0d21a-106">The **Get-AzureRmVMCustomScriptExtension** cmdlet gets information about a custom script Virtual Machine Extension on a virtual machine.</span></span>

## <span data-ttu-id="0d21a-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0d21a-107">EXAMPLES</span></span>

### <span data-ttu-id="0d21a-108">Örnek 1: özel bir komut dosyası uzantısı alma</span><span class="sxs-lookup"><span data-stu-id="0d21a-108">Example 1: Get a custom script extension</span></span>
```
PS C:\> $VMCustomScriptExtension = Get-AzureRmVMCustomScriptExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoCustomScript"
```

<span data-ttu-id="0d21a-109">Bu komut, VirtualMachine07 adındaki sanal makine için ContosoCustomScript adındaki özel komut dosyası uzantısını alır.</span><span class="sxs-lookup"><span data-stu-id="0d21a-109">This command gets the custom script extension named ContosoCustomScript for the virtual machine named VirtualMachine07.</span></span>

### <span data-ttu-id="0d21a-110">Örnek 2: özel bir komut dosyası uzantısının örnek görünümünü alma</span><span class="sxs-lookup"><span data-stu-id="0d21a-110">Example 2: Get the instance view of a custom script extension</span></span>
```
PS C:\> $VMCustomScriptExtension = Get-AzureRmVMCustomScriptExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoCustomScript" -Status
```

<span data-ttu-id="0d21a-111">Bu komut, VirtualMachine07 adındaki sanal makine için ContosoCustomScript adındaki özel komut dosyası uzantısının örnek görünümünü alır.</span><span class="sxs-lookup"><span data-stu-id="0d21a-111">This command gets the instance view of the custom script extension named ContosoCustomScript for the virtual machine named VirtualMachine07.</span></span>

## <span data-ttu-id="0d21a-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0d21a-112">PARAMETERS</span></span>

### <span data-ttu-id="0d21a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d21a-113">-DefaultProfile</span></span>
<span data-ttu-id="0d21a-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0d21a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0d21a-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="0d21a-115">-Name</span></span>
<span data-ttu-id="0d21a-116">Bu cmdlet 'in bilgi aldığı özel komut dosyası uzantısının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0d21a-116">Specifies the name of the custom script extension about which this cmdlet gets information.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d21a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d21a-117">-ResourceGroupName</span></span>
<span data-ttu-id="0d21a-118">Sanal makinenin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0d21a-118">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="0d21a-119">-Durum</span><span class="sxs-lookup"><span data-stu-id="0d21a-119">-Status</span></span>
<span data-ttu-id="0d21a-120">Bu cmdlet 'in özel betik uzantısının örnek görünümünü aldığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0d21a-120">Indicates that this cmdlet gets the instance view of the custom script extension.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d21a-121">-VMName</span><span class="sxs-lookup"><span data-stu-id="0d21a-121">-VMName</span></span>
<span data-ttu-id="0d21a-122">Bu cmdlet 'in özel komut dosyası uzantısını aldığı sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0d21a-122">Specifies the name of a virtual machine for which this cmdlet gets the custom script extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d21a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d21a-123">CommonParameters</span></span>
<span data-ttu-id="0d21a-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0d21a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d21a-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d21a-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d21a-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0d21a-126">INPUTS</span></span>

## <span data-ttu-id="0d21a-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0d21a-127">OUTPUTS</span></span>

## <span data-ttu-id="0d21a-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0d21a-128">NOTES</span></span>

## <span data-ttu-id="0d21a-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0d21a-129">RELATED LINKS</span></span>

[<span data-ttu-id="0d21a-130">Get-Azurermvmaccessextenma</span><span class="sxs-lookup"><span data-stu-id="0d21a-130">Get-AzureRmVMAccessExtension</span></span>](./Get-AzureRmVMAccessExtension.md)

[<span data-ttu-id="0d21a-131">Get-Azurermvmexgeri</span><span class="sxs-lookup"><span data-stu-id="0d21a-131">Get-AzureRmVMExtension</span></span>](./Get-AzureRmVMExtension.md)

[<span data-ttu-id="0d21a-132">Get-Azurermvmextensionımage</span><span class="sxs-lookup"><span data-stu-id="0d21a-132">Get-AzureRmVMExtensionImage</span></span>](./Get-AzureRmVMExtensionImage.md)


