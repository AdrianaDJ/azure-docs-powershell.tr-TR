---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/disable-azurermvmssdiskencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Disable-AzureRmVmssDiskEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Disable-AzureRmVmssDiskEncryption.md
ms.openlocfilehash: 7ff2512fa7c6247d75eb8b288c888dc2aff670dd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590523"
---
# <span data-ttu-id="79845-101">Disable-AzureRmVmssDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="79845-101">Disable-AzureRmVmssDiskEncryption</span></span>

## <span data-ttu-id="79845-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="79845-102">SYNOPSIS</span></span>
<span data-ttu-id="79845-103">VM ölçeklendirme kümesinde disk şifrelemesini devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="79845-103">Disables disk encryption on a VM scale set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="79845-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="79845-104">SYNTAX</span></span>

```
Disable-AzureRmVmssDiskEncryption [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [[-ExtensionName] <String>] [-VolumeType <String>] [-ForceUpdate] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="79845-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="79845-105">DESCRIPTION</span></span>
<span data-ttu-id="79845-106">VM ölçeklendirme kümesinde disk şifrelemesini devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="79845-106">Disables disk encryption on a VM scale set.</span></span>

## <span data-ttu-id="79845-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="79845-107">EXAMPLES</span></span>

### <span data-ttu-id="79845-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="79845-108">Example 1</span></span>
```
PS C:\> Disable-AzureRmVmssDiskEncryption -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="79845-109">Group001 adındaki kaynak grubuna ait olan VMSS001 adlı VM Ölçek kümesindeki disk şifrelemesini devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="79845-109">Disables disk encryption on the VM scale set named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="79845-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="79845-110">PARAMETERS</span></span>

### <span data-ttu-id="79845-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="79845-111">-AsJob</span></span>
<span data-ttu-id="79845-112">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="79845-112">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79845-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79845-113">-DefaultProfile</span></span>
<span data-ttu-id="79845-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="79845-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="79845-115">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="79845-115">-ExtensionName</span></span>
<span data-ttu-id="79845-116">Uzantı adı.</span><span class="sxs-lookup"><span data-stu-id="79845-116">The extension name.</span></span>
<span data-ttu-id="79845-117">Bu parametre belirtilmezse, kullanılan varsayılan değerler Windows VM 'ler için AzureDiskEncryption ve Linux VM 'Ler için AzureDiskEncryptionForLinux.</span><span class="sxs-lookup"><span data-stu-id="79845-117">If this parameter is not specified, default values used are AzureDiskEncryption for windows VMs and AzureDiskEncryptionForLinux for Linux VMs.</span></span>

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

### <span data-ttu-id="79845-118">-Force</span><span class="sxs-lookup"><span data-stu-id="79845-118">-Force</span></span>
<span data-ttu-id="79845-119">Sanal makineden uzantının kaldırılmasını zorlamak için.</span><span class="sxs-lookup"><span data-stu-id="79845-119">To force the removal of the extension from the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79845-120">-ForceUpdate</span><span class="sxs-lookup"><span data-stu-id="79845-120">-ForceUpdate</span></span>
<span data-ttu-id="79845-121">Zorla güncelleştirmesi için bir etiket oluşturun.</span><span class="sxs-lookup"><span data-stu-id="79845-121">Generate a tag for force update.</span></span>  <span data-ttu-id="79845-122">Bu, aynı VM 'de yinelenen şifreleme işlemleri gerçekleştirmek için verilmelidir.</span><span class="sxs-lookup"><span data-stu-id="79845-122">This should be given to perform repeated encryption operations on the same VM.</span></span>

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

### <span data-ttu-id="79845-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79845-123">-ResourceGroupName</span></span>
<span data-ttu-id="79845-124">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="79845-124">The resource group name.</span></span>

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

### <span data-ttu-id="79845-125">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="79845-125">-VMScaleSetName</span></span>
<span data-ttu-id="79845-126">Sanal makine adı.</span><span class="sxs-lookup"><span data-stu-id="79845-126">The virtual machine name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79845-127">-Birimtürü</span><span class="sxs-lookup"><span data-stu-id="79845-127">-VolumeType</span></span>
<span data-ttu-id="79845-128">Şifreleme işlemi gerçekleştirmek için birimin türü (OS veya veri)</span><span class="sxs-lookup"><span data-stu-id="79845-128">Type of the volume (OS or Data) to perform encryption operation</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: OS, Data, All

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79845-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="79845-129">-Confirm</span></span>
<span data-ttu-id="79845-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="79845-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79845-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79845-131">-WhatIf</span></span>
<span data-ttu-id="79845-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="79845-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="79845-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="79845-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79845-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79845-134">CommonParameters</span></span>
<span data-ttu-id="79845-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="79845-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79845-136">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79845-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79845-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="79845-137">INPUTS</span></span>

### <span data-ttu-id="79845-138">System. String</span><span class="sxs-lookup"><span data-stu-id="79845-138">System.String</span></span>

## <span data-ttu-id="79845-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="79845-139">OUTPUTS</span></span>

### <span data-ttu-id="79845-140">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="79845-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="79845-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="79845-141">NOTES</span></span>

## <span data-ttu-id="79845-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="79845-142">RELATED LINKS</span></span>
