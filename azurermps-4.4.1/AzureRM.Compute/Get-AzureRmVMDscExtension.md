---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 5B7A1BE6-F5F5-4968-BE32-7743D0E25FE3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMDscExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMDscExtension.md
ms.openlocfilehash: ea54fc227fb32fe945a7a5ccc33133fc3b1d98a0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592649"
---
# <span data-ttu-id="42544-101">Get-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="42544-101">Get-AzureRmVMDscExtension</span></span>

## <span data-ttu-id="42544-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="42544-102">SYNOPSIS</span></span>
<span data-ttu-id="42544-103">Belirli bir sanal makinedeki DSC uzantısının ayarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="42544-103">Gets the settings of the DSC extension on a particular virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="42544-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="42544-104">SYNTAX</span></span>

```
Get-AzureRmVMDscExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="42544-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="42544-105">DESCRIPTION</span></span>
<span data-ttu-id="42544-106">**Get-AzureRmVMDscExtension** cmdlet 'i, belirli bir sanal makinede Istenen durum YAPıLANDıRMASı (DSC) uzantısının ayarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="42544-106">The **Get-AzureRmVMDscExtension** cmdlet gets the settings of the Desired State Configuration (DSC) extension on a particular virtual machine.</span></span>

## <span data-ttu-id="42544-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="42544-107">EXAMPLES</span></span>

### <span data-ttu-id="42544-108">Örnek 1: DSC uzantısının ayarlarını alma</span><span class="sxs-lookup"><span data-stu-id="42544-108">Example 1: Get the settings of a DSC extension</span></span>
```
PS C:\> Get-AzureRmVMDscExtension -ResourceGroupName "ResourceGroup002" -VMName "VM07" -Name "DSC"
```

<span data-ttu-id="42544-109">Bu komut, VM07 adındaki sanal makinede DSC adlı uzantının ayarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="42544-109">This command gets the settings of extension named DSC on the virtual machine named VM07.</span></span>

## <span data-ttu-id="42544-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="42544-110">PARAMETERS</span></span>

### <span data-ttu-id="42544-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42544-111">-DefaultProfile</span></span>
<span data-ttu-id="42544-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="42544-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="42544-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="42544-113">-Name</span></span>
<span data-ttu-id="42544-114">Uzantıyı temsil eden Azure Resource Manager kaynağının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="42544-114">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="42544-115">Set-AzureRmVMDscExtension cmdlet, **Get-AzureRmVMDscExtension** tarafından kullanılan değer olan Microsoft. POWERSHELL. DSC olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="42544-115">The Set-AzureRmVMDscExtension cmdlet sets this name to Microsoft.Powershell.DSC, which is the same value that is used by **Get-AzureRmVMDscExtension**.</span></span>
<span data-ttu-id="42544-116">Bu parametreyi yalnızca **set-AzureRmVMDscExtension** cmdlet 'inde varsayılan adı değiştirdiyseniz veya Kaynak Yöneticisi şablonunda farklı bir kaynak adı kullandıysanız belirtin.</span><span class="sxs-lookup"><span data-stu-id="42544-116">Specify this parameter only if you changed the default name in the **Set-AzureRmVMDscExtension** cmdlet or used a different resource name in a Resource Manager template.</span></span>

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

### <span data-ttu-id="42544-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42544-117">-ResourceGroupName</span></span>
<span data-ttu-id="42544-118">Sanal makinenin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="42544-118">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="42544-119">-Durum</span><span class="sxs-lookup"><span data-stu-id="42544-119">-Status</span></span>
<span data-ttu-id="42544-120">Bu cmdlet 'in DSC uzantısının örnek görünümünü aldığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="42544-120">Indicates that this cmdlet gets the instance view of the DSC extension.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42544-121">-VMName</span><span class="sxs-lookup"><span data-stu-id="42544-121">-VMName</span></span>
<span data-ttu-id="42544-122">Bu cmdlet 'in DSC uzantısını aldığı sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="42544-122">Specifies the name of a virtual machine for which this cmdlet gets the DSC extension.</span></span>

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

### <span data-ttu-id="42544-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42544-123">CommonParameters</span></span>
<span data-ttu-id="42544-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="42544-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42544-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42544-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42544-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="42544-126">INPUTS</span></span>

## <span data-ttu-id="42544-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="42544-127">OUTPUTS</span></span>

### <span data-ttu-id="42544-128">Microsoft. Azure. Commands. COMPUTE. Extension. DSC. VirtualMachineDscExtensionContext</span><span class="sxs-lookup"><span data-stu-id="42544-128">Microsoft.Azure.Commands.Compute.Extension.DSC.VirtualMachineDscExtensionContext</span></span>

## <span data-ttu-id="42544-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="42544-129">NOTES</span></span>

## <span data-ttu-id="42544-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="42544-130">RELATED LINKS</span></span>

[<span data-ttu-id="42544-131">Remove-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="42544-131">Remove-AzureRmVMDscExtension</span></span>](./Remove-AzureRmVMDscExtension.md)

[<span data-ttu-id="42544-132">Set-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="42544-132">Set-AzureRmVMDscExtension</span></span>](./Set-AzureRmVMDscExtension.md)


