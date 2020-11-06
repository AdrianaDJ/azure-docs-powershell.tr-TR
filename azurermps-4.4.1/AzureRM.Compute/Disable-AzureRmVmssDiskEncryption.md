---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Disable-AzureRmVmssDiskEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Disable-AzureRmVmssDiskEncryption.md
ms.openlocfilehash: 8cb68b45637496cb87e387c6755fe861fe3e21f6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594797"
---
# <span data-ttu-id="ec27a-101">Disable-AzureRmVmssDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="ec27a-101">Disable-AzureRmVmssDiskEncryption</span></span>

## <span data-ttu-id="ec27a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ec27a-102">SYNOPSIS</span></span>
<span data-ttu-id="ec27a-103">VM ölçeklendirme kümesinde disk şifrelemesini devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="ec27a-103">Disables disk encryption on a VM scale set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ec27a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ec27a-104">SYNTAX</span></span>

```
Disable-AzureRmVmssDiskEncryption [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [[-ExtensionName] <String>] [-VolumeType <String>] [-ForceUpdate] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ec27a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ec27a-105">DESCRIPTION</span></span>
<span data-ttu-id="ec27a-106">VM ölçeklendirme kümesinde disk şifrelemesini devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="ec27a-106">Disables disk encryption on a VM scale set.</span></span>

## <span data-ttu-id="ec27a-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ec27a-107">EXAMPLES</span></span>

### <span data-ttu-id="ec27a-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="ec27a-108">Example 1</span></span>
```
PS C:\> Disable-AzureRmVmssDiskEncryption -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="ec27a-109">Group001 adındaki kaynak grubuna ait olan VMSS001 adlı VM Ölçek kümesindeki disk şifrelemesini devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="ec27a-109">Disables disk encryption on the VM scale set named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="ec27a-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ec27a-110">PARAMETERS</span></span>

### <span data-ttu-id="ec27a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec27a-111">-DefaultProfile</span></span>
<span data-ttu-id="ec27a-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ec27a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ec27a-113">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="ec27a-113">-ExtensionName</span></span>
<span data-ttu-id="ec27a-114">Uzantı adı.</span><span class="sxs-lookup"><span data-stu-id="ec27a-114">The extension name.</span></span>
<span data-ttu-id="ec27a-115">Bu parametre belirtilmezse, kullanılan varsayılan değerler Windows VM 'ler için AzureDiskEncryption ve Linux VM 'Ler için AzureDiskEncryptionForLinux.</span><span class="sxs-lookup"><span data-stu-id="ec27a-115">If this parameter is not specified, default values used are AzureDiskEncryption for windows VMs and AzureDiskEncryptionForLinux for Linux VMs.</span></span>

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

### <span data-ttu-id="ec27a-116">-Force</span><span class="sxs-lookup"><span data-stu-id="ec27a-116">-Force</span></span>
<span data-ttu-id="ec27a-117">Sanal makineden uzantının kaldırılmasını zorlamak için.</span><span class="sxs-lookup"><span data-stu-id="ec27a-117">To force the removal of the extension from the virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec27a-118">-ForceUpdate</span><span class="sxs-lookup"><span data-stu-id="ec27a-118">-ForceUpdate</span></span>
<span data-ttu-id="ec27a-119">Zorla güncelleştirmesi için bir etiket oluşturun.</span><span class="sxs-lookup"><span data-stu-id="ec27a-119">Generate a tag for force update.</span></span>  <span data-ttu-id="ec27a-120">Bu, aynı VM 'de yinelenen şifreleme işlemleri gerçekleştirmek için verilmelidir.</span><span class="sxs-lookup"><span data-stu-id="ec27a-120">This should be given to perform repeated encryption operations on the same VM.</span></span>

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

### <span data-ttu-id="ec27a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec27a-121">-ResourceGroupName</span></span>
<span data-ttu-id="ec27a-122">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="ec27a-122">The resource group name.</span></span>

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

### <span data-ttu-id="ec27a-123">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="ec27a-123">-VMScaleSetName</span></span>
<span data-ttu-id="ec27a-124">Sanal makine adı.</span><span class="sxs-lookup"><span data-stu-id="ec27a-124">The virtual machine name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec27a-125">-Birimtürü</span><span class="sxs-lookup"><span data-stu-id="ec27a-125">-VolumeType</span></span>
<span data-ttu-id="ec27a-126">Şifreleme işlemi gerçekleştirmek için birimin türü (OS veya veri)</span><span class="sxs-lookup"><span data-stu-id="ec27a-126">Type of the volume (OS or Data) to perform encryption operation</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: OS, Data, All

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec27a-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="ec27a-127">-Confirm</span></span>
<span data-ttu-id="ec27a-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ec27a-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec27a-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ec27a-129">-WhatIf</span></span>
<span data-ttu-id="ec27a-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ec27a-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ec27a-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ec27a-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec27a-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec27a-132">CommonParameters</span></span>
<span data-ttu-id="ec27a-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ec27a-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec27a-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ec27a-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec27a-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ec27a-135">INPUTS</span></span>

### <span data-ttu-id="ec27a-136">System. String</span><span class="sxs-lookup"><span data-stu-id="ec27a-136">System.String</span></span>

## <span data-ttu-id="ec27a-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ec27a-137">OUTPUTS</span></span>

### <span data-ttu-id="ec27a-138">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="ec27a-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="ec27a-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ec27a-139">NOTES</span></span>

## <span data-ttu-id="ec27a-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ec27a-140">RELATED LINKS</span></span>

