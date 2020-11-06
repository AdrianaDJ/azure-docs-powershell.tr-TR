---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmssvmdiskencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVmssVMDiskEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVmssVMDiskEncryption.md
ms.openlocfilehash: c45574272d814ea899e7d291b729b6a8e6526da6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587619"
---
# <span data-ttu-id="686b6-101">Get-AzureRmVmssVMDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="686b6-101">Get-AzureRmVmssVMDiskEncryption</span></span>

## <span data-ttu-id="686b6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="686b6-102">SYNOPSIS</span></span>
<span data-ttu-id="686b6-103">VM Ölçek kümesindeki VM 'lerin disk şifreleme durumunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="686b6-103">Shows the disk encryption status of VMs in a VM scale set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="686b6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="686b6-104">SYNTAX</span></span>

```
Get-AzureRmVmssVMDiskEncryption [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [[-InstanceId] <String>] [-ExtensionName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="686b6-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="686b6-105">DESCRIPTION</span></span>
<span data-ttu-id="686b6-106">VM Ölçek kümesinin disk şifreleme durumunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="686b6-106">Shows the disk encryption status of VM scale set.</span></span>

## <span data-ttu-id="686b6-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="686b6-107">EXAMPLES</span></span>

### <span data-ttu-id="686b6-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="686b6-108">Example 1</span></span>
```
PS C:\> Get-AzureRmVmssVMDiskEncryption -ResourceGroupName "Group001" -VMScaleSetName "VMSS001" -InstanceId "1"
```

<span data-ttu-id="686b6-109">Group001 adındaki kaynak grubuna ait VMSS001 adındaki VM Ölçek kümesindeki VM örneğinin disk şifreleme durumunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="686b6-109">Shows the disk encryption status of VM instance 1 in the VM scale set named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="686b6-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="686b6-110">PARAMETERS</span></span>

### <span data-ttu-id="686b6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="686b6-111">-DefaultProfile</span></span>
<span data-ttu-id="686b6-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="686b6-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="686b6-113">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="686b6-113">-ExtensionName</span></span>
<span data-ttu-id="686b6-114">Uzantı adı.</span><span class="sxs-lookup"><span data-stu-id="686b6-114">The extension name.</span></span>
<span data-ttu-id="686b6-115">Bu parametre belirtilmezse, kullanılan varsayılan değerler Windows VM 'ler için AzureDiskEncryption ve Linux VM 'Ler için AzureDiskEncryptionForLinux.</span><span class="sxs-lookup"><span data-stu-id="686b6-115">If this parameter is not specified, default values used are AzureDiskEncryption for windows VMs and AzureDiskEncryptionForLinux for Linux VMs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="686b6-116">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="686b6-116">-InstanceId</span></span>
<span data-ttu-id="686b6-117">Örnek KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="686b6-117">Specifies the instance ID.</span></span>

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

### <span data-ttu-id="686b6-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="686b6-118">-ResourceGroupName</span></span>
<span data-ttu-id="686b6-119">Sanal makine ölçek kümesinin kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="686b6-119">Resource group name of the virtual machine scale set.</span></span>

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

### <span data-ttu-id="686b6-120">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="686b6-120">-VMScaleSetName</span></span>
<span data-ttu-id="686b6-121">Sanal makine ölçek kümesi adı.</span><span class="sxs-lookup"><span data-stu-id="686b6-121">The virtual machine scale set name.</span></span>

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

### <span data-ttu-id="686b6-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="686b6-122">CommonParameters</span></span>
<span data-ttu-id="686b6-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="686b6-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="686b6-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="686b6-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="686b6-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="686b6-125">INPUTS</span></span>

### <span data-ttu-id="686b6-126">System. String</span><span class="sxs-lookup"><span data-stu-id="686b6-126">System.String</span></span>

## <span data-ttu-id="686b6-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="686b6-127">OUTPUTS</span></span>

### <span data-ttu-id="686b6-128">Microsoft. Azure. Commands. COMPUTE. modeller. PSVmssVMDiskEncryptionStatusContext</span><span class="sxs-lookup"><span data-stu-id="686b6-128">Microsoft.Azure.Commands.Compute.Models.PSVmssVMDiskEncryptionStatusContext</span></span>

## <span data-ttu-id="686b6-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="686b6-129">NOTES</span></span>

## <span data-ttu-id="686b6-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="686b6-130">RELATED LINKS</span></span>
