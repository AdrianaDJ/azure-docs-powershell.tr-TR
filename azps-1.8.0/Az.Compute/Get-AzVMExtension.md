---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 842652D4-0F1C-4D0D-AB55-0D43D3C5D82A
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMExtension.md
ms.openlocfilehash: f861465fcc9f27f71142ffd4e49935039f3da9c0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93761344"
---
# <span data-ttu-id="c5d6a-101">Get-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="c5d6a-101">Get-AzVMExtension</span></span>

## <span data-ttu-id="c5d6a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c5d6a-102">SYNOPSIS</span></span>
<span data-ttu-id="c5d6a-103">Sanal makinede yüklü sanal makine uzantılarının özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="c5d6a-103">Gets properties of Virtual Machine Extensions installed on a virtual machine.</span></span>

## <span data-ttu-id="c5d6a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c5d6a-104">SYNTAX</span></span>

```
Get-AzVMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c5d6a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c5d6a-105">DESCRIPTION</span></span>
<span data-ttu-id="c5d6a-106">**Get-Azvmexter** cmdlet 'i, sanal makinede yüklü sanal makine uzantılarının özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="c5d6a-106">The **Get-AzVMExtension** cmdlet gets properties of Virtual Machine Extensions installed on a virtual machine.</span></span>
<span data-ttu-id="c5d6a-107">Özelliklerini almak istediğiniz uzantının adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="c5d6a-107">Specify the name of an extension for which to get properties.</span></span>
<span data-ttu-id="c5d6a-108">Bir uzantının yalnızca örnek görünümüne ulaşmak için, durum parametresini belirtin.</span><span class="sxs-lookup"><span data-stu-id="c5d6a-108">To get only the instance view of an extension, specify the Status parameter.</span></span>

## <span data-ttu-id="c5d6a-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c5d6a-109">EXAMPLES</span></span>

### <span data-ttu-id="c5d6a-110">Örnek 1: bir uzantının özelliklerini alma</span><span class="sxs-lookup"><span data-stu-id="c5d6a-110">Example 1: Get properties of an extension</span></span>
```
PS C:\> Get-AzVMExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine22" -Name "CustomScriptExtension"

ResourceGroupName       : ResourceGroup11
VMName                  : VirtualMachine22
Name                    : CustomScriptExtension
Location                : eastus
Etag                    : null
Publisher               : Microsoft.Azure.Extensions
ExtensionType           : CustomScript
TypeHandlerVersion      : 2.0
Id                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup11
                          /providers/Microsoft.Compute/virtualMachines/VirtualMachine22/extensions/CustomScriptExtension
PublicSettings          : {}
ProtectedSettings       :
ProvisioningState       : Succeeded
Statuses                :
SubStatuses             :
AutoUpgradeMinorVersion : True
ForceUpdateTag          :
```

<span data-ttu-id="c5d6a-111">Bu komut ResourceGroup11 kaynak grubundaki VirtualMachine22 adındaki sanal makinede CustomScriptExtension adlı uzantının özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="c5d6a-111">This command gets properties for the extension named CustomScriptExtension on the virtual machine named VirtualMachine22 in the resource group ResourceGroup11.</span></span>

### <span data-ttu-id="c5d6a-112">Örnek 2: uzantının örnek görünümünü alma</span><span class="sxs-lookup"><span data-stu-id="c5d6a-112">Example 2: Get instance view of an extension</span></span>
```
PS C:\> Get-AzVMExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine22" -Name "CustomScriptExtension" -Status

ResourceGroupName       : ResourceGroup11
VMName                  : VirtualMachine22
Name                    : CustomScriptExtension
Location                : eastus
Etag                    : null
Publisher               : Microsoft.Azure.Extensions
ExtensionType           : CustomScript
TypeHandlerVersion      : 2.0
Id                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup11
                          /providers/Microsoft.Compute/virtualMachines/VirtualMachine22/extensions/CustomScriptExtension
PublicSettings          : {}
ProtectedSettings       :
ProvisioningState       : Succeeded
Statuses                : {Microsoft.Azure.Management.Compute.Models.InstanceViewStatus}
SubStatuses             :
AutoUpgradeMinorVersion : True
ForceUpdateTag          :
```

<span data-ttu-id="c5d6a-113">Bu komut, kaynak grubundaki ResourceGroup11 VirtualMachine22 adındaki sanal makinede CustomScriptExtension adlı uzantının örnek görünümünü alır.</span><span class="sxs-lookup"><span data-stu-id="c5d6a-113">This command gets the instance view for the extension named CustomScriptExtension on the virtual machine named VirtualMachine22 in the resource group ResourceGroup11.</span></span>

### <span data-ttu-id="c5d6a-114">Örnek 3: VM 'de yüklü tüm uzantıları alma</span><span class="sxs-lookup"><span data-stu-id="c5d6a-114">Example 3: Get all extensions installed on a VM</span></span>
```
PS C:\> Get-AzVMExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine22"

ResourceGroupName       : ResourceGroup11
VMName                  : VirtualMachine22
Name                    : CustomScriptExtension
Location                : eastus
Etag                    : null
Publisher               : Microsoft.Azure.Extensions
ExtensionType           : CustomScript
TypeHandlerVersion      : 2.0
Id                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup11
                          /providers/Microsoft.Compute/virtualMachines/VirtualMachine22/extensions/CustomScriptExtension
PublicSettings          : {}
ProtectedSettings       :
ProvisioningState       : Succeeded
Statuses                :
SubStatuses             :
AutoUpgradeMinorVersion : True
ForceUpdateTag          :
```

<span data-ttu-id="c5d6a-115">Bu komut, kaynak grubundaki VirtualMachine22 adındaki sanal makinede yüklü olan uzantıların listesini alır.</span><span class="sxs-lookup"><span data-stu-id="c5d6a-115">This command gets the list of extensions installed on the virtual machine named VirtualMachine22 in the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="c5d6a-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c5d6a-116">PARAMETERS</span></span>

### <span data-ttu-id="c5d6a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5d6a-117">-DefaultProfile</span></span>
<span data-ttu-id="c5d6a-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c5d6a-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c5d6a-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="c5d6a-119">-Name</span></span>
<span data-ttu-id="c5d6a-120">Bir uzantının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c5d6a-120">Specifies the name of an extension.</span></span>
<span data-ttu-id="c5d6a-121">Bu cmdlet, bu parametrenin belirttiği uzantının özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="c5d6a-121">This cmdlet gets properties for the extension that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5d6a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5d6a-122">-ResourceGroupName</span></span>
<span data-ttu-id="c5d6a-123">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c5d6a-123">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="c5d6a-124">-Durum</span><span class="sxs-lookup"><span data-stu-id="c5d6a-124">-Status</span></span>
<span data-ttu-id="c5d6a-125">Bu cmdlet 'in yalnızca bir uzantının örnek görünümünü aldığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c5d6a-125">Indicates that this cmdlet gets only the instance view of an extension.</span></span>

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

### <span data-ttu-id="c5d6a-126">-VMName</span><span class="sxs-lookup"><span data-stu-id="c5d6a-126">-VMName</span></span>
<span data-ttu-id="c5d6a-127">Sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c5d6a-127">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="c5d6a-128">Bu cmdlet, bu parametrenin belirttiği sanal makineden uzantının özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="c5d6a-128">This cmdlet gets properties of an extension from the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="c5d6a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5d6a-129">CommonParameters</span></span>
<span data-ttu-id="c5d6a-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c5d6a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5d6a-131">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="c5d6a-131">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5d6a-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c5d6a-132">INPUTS</span></span>

### <span data-ttu-id="c5d6a-133">System. String</span><span class="sxs-lookup"><span data-stu-id="c5d6a-133">System.String</span></span>

### <span data-ttu-id="c5d6a-134">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="c5d6a-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="c5d6a-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c5d6a-135">OUTPUTS</span></span>

### <span data-ttu-id="c5d6a-136">Microsoft. Azure. Commands. COMPUTE. modeller. PSVirtualMachineExtension</span><span class="sxs-lookup"><span data-stu-id="c5d6a-136">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtension</span></span>

## <span data-ttu-id="c5d6a-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c5d6a-137">NOTES</span></span>

## <span data-ttu-id="c5d6a-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c5d6a-138">RELATED LINKS</span></span>

[<span data-ttu-id="c5d6a-139">Remove-Azvmexgergeri</span><span class="sxs-lookup"><span data-stu-id="c5d6a-139">Remove-AzVMExtension</span></span>](./Remove-AzVMExtension.md)

[<span data-ttu-id="c5d6a-140">Set-Azvmexgeri</span><span class="sxs-lookup"><span data-stu-id="c5d6a-140">Set-AzVMExtension</span></span>](./Set-AzVMExtension.md)


