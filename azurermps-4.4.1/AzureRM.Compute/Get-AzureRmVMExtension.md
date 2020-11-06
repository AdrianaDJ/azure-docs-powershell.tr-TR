---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 842652D4-0F1C-4D0D-AB55-0D43D3C5D82A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMExtension.md
ms.openlocfilehash: 9ec51984a4b8291f726da81b92b1c67ea8937e5e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592644"
---
# <span data-ttu-id="3c543-101">Get-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="3c543-101">Get-AzureRmVMExtension</span></span>

## <span data-ttu-id="3c543-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3c543-102">SYNOPSIS</span></span>
<span data-ttu-id="3c543-103">Sanal makinede yüklü sanal makine uzantılarının özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="3c543-103">Gets properties of Virtual Machine Extensions installed on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3c543-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3c543-104">SYNTAX</span></span>

```
Get-AzureRmVMExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3c543-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="3c543-105">DESCRIPTION</span></span>
<span data-ttu-id="3c543-106">**Get-Azurermvmexter** cmdlet 'i, sanal makinede yüklü sanal makine uzantılarının özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="3c543-106">The **Get-AzureRmVMExtension** cmdlet gets properties of Virtual Machine Extensions installed on a virtual machine.</span></span>
<span data-ttu-id="3c543-107">Özelliklerini almak istediğiniz uzantının adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="3c543-107">Specify the name of an extension for which to get properties.</span></span>
<span data-ttu-id="3c543-108">Bir uzantının yalnızca örnek görünümüne ulaşmak için, durum parametresini belirtin.</span><span class="sxs-lookup"><span data-stu-id="3c543-108">To get only the instance view of an extension, specify the Status parameter.</span></span>

## <span data-ttu-id="3c543-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3c543-109">EXAMPLES</span></span>

### <span data-ttu-id="3c543-110">Örnek 1: bir uzantının özelliklerini alma</span><span class="sxs-lookup"><span data-stu-id="3c543-110">Example 1: Get properties of an extension</span></span>
```
PS C:\> Get-AzureRmVMExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine22" -Name "CustomScriptExtension"
```

<span data-ttu-id="3c543-111">Bu komut ResourceGroup11 kaynak grubundaki VirtualMachine22 adındaki sanal makinede CustomScriptExtension adlı uzantının özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="3c543-111">This command gets properties for the extension named CustomScriptExtension on the virtual machine named VirtualMachine22 in the resource group ResourceGroup11.</span></span>

### <span data-ttu-id="3c543-112">Örnek 2: uzantının örnek görünümünü alma</span><span class="sxs-lookup"><span data-stu-id="3c543-112">Example 2: Get instance view of an extension</span></span>
```
PS C:\> Get-AzureRmVMExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine22" -Name "CustomScriptExtension" -Status
```

<span data-ttu-id="3c543-113">Bu komut, kaynak grubundaki ResourceGroup11 VirtualMachine22 adındaki sanal makinede CustomScriptExtension adlı uzantının örnek görünümünü alır.</span><span class="sxs-lookup"><span data-stu-id="3c543-113">This command gets the instance view for the extension named CustomScriptExtension on the virtual machine named VirtualMachine22 in the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="3c543-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3c543-114">PARAMETERS</span></span>

### <span data-ttu-id="3c543-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c543-115">-DefaultProfile</span></span>
<span data-ttu-id="3c543-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3c543-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3c543-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="3c543-117">-Name</span></span>
<span data-ttu-id="3c543-118">Bir uzantının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3c543-118">Specifies the name of an extension.</span></span>
<span data-ttu-id="3c543-119">Bu cmdlet, bu parametrenin belirttiği uzantının özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="3c543-119">This cmdlet gets properties for the extension that this parameter specifies.</span></span>

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

### <span data-ttu-id="3c543-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c543-120">-ResourceGroupName</span></span>
<span data-ttu-id="3c543-121">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3c543-121">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="3c543-122">-Durum</span><span class="sxs-lookup"><span data-stu-id="3c543-122">-Status</span></span>
<span data-ttu-id="3c543-123">Bu cmdlet 'in yalnızca bir uzantının örnek görünümünü aldığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3c543-123">Indicates that this cmdlet gets only the instance view of an extension.</span></span>

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

### <span data-ttu-id="3c543-124">-VMName</span><span class="sxs-lookup"><span data-stu-id="3c543-124">-VMName</span></span>
<span data-ttu-id="3c543-125">Sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3c543-125">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="3c543-126">Bu cmdlet, bu parametrenin belirttiği sanal makineden uzantının özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="3c543-126">This cmdlet gets properties of an extension from the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="3c543-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c543-127">CommonParameters</span></span>
<span data-ttu-id="3c543-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3c543-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c543-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3c543-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c543-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3c543-130">INPUTS</span></span>

## <span data-ttu-id="3c543-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3c543-131">OUTPUTS</span></span>

## <span data-ttu-id="3c543-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3c543-132">NOTES</span></span>

## <span data-ttu-id="3c543-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3c543-133">RELATED LINKS</span></span>

[<span data-ttu-id="3c543-134">Remove-Azurermvmexgeri</span><span class="sxs-lookup"><span data-stu-id="3c543-134">Remove-AzureRmVMExtension</span></span>](./Remove-AzureRmVMExtension.md)

[<span data-ttu-id="3c543-135">Set-Azurermvmexgeri</span><span class="sxs-lookup"><span data-stu-id="3c543-135">Set-AzureRmVMExtension</span></span>](./Set-AzureRmVMExtension.md)


