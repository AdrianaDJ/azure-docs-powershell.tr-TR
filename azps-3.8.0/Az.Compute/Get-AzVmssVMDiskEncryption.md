---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmssvmdiskencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssVMDiskEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssVMDiskEncryption.md
ms.openlocfilehash: 8ff3ad92f976e6a8af9c4a24e143ed3859832d35
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096406"
---
# <span data-ttu-id="62807-101">Get-AzVmssVMDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="62807-101">Get-AzVmssVMDiskEncryption</span></span>

## <span data-ttu-id="62807-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="62807-102">SYNOPSIS</span></span>
<span data-ttu-id="62807-103">VM Ölçek kümesindeki VM 'lerin disk şifreleme durumunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="62807-103">Shows the disk encryption status of VMs in a VM scale set.</span></span>

## <span data-ttu-id="62807-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="62807-104">SYNTAX</span></span>

```
Get-AzVmssVMDiskEncryption [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String>]
 [-ExtensionName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="62807-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="62807-105">DESCRIPTION</span></span>
<span data-ttu-id="62807-106">VM Ölçek kümesinin disk şifreleme durumunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="62807-106">Shows the disk encryption status of VM scale set.</span></span>

## <span data-ttu-id="62807-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="62807-107">EXAMPLES</span></span>

### <span data-ttu-id="62807-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="62807-108">Example 1</span></span>
```
PS C:\> Get-AzVmssVMDiskEncryption -ResourceGroupName "Group001" -VMScaleSetName "VMSS001" -InstanceId "1"
```

<span data-ttu-id="62807-109">Group001 adındaki kaynak grubuna ait VMSS001 adındaki VM Ölçek kümesindeki VM örneğinin disk şifreleme durumunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="62807-109">Shows the disk encryption status of VM instance 1 in the VM scale set named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="62807-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="62807-110">PARAMETERS</span></span>

### <span data-ttu-id="62807-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62807-111">-DefaultProfile</span></span>
<span data-ttu-id="62807-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="62807-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="62807-113">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="62807-113">-ExtensionName</span></span>
<span data-ttu-id="62807-114">Uzantı adı.</span><span class="sxs-lookup"><span data-stu-id="62807-114">The extension name.</span></span>
<span data-ttu-id="62807-115">Bu parametre belirtilmezse, kullanılan varsayılan değerler Windows VM 'ler için AzureDiskEncryption ve Linux VM 'Ler için AzureDiskEncryptionForLinux.</span><span class="sxs-lookup"><span data-stu-id="62807-115">If this parameter is not specified, default values used are AzureDiskEncryption for windows VMs and AzureDiskEncryptionForLinux for Linux VMs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62807-116">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="62807-116">-InstanceId</span></span>
<span data-ttu-id="62807-117">Örnek KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="62807-117">Specifies the instance ID.</span></span>

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

### <span data-ttu-id="62807-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62807-118">-ResourceGroupName</span></span>
<span data-ttu-id="62807-119">Sanal makine ölçek kümesinin kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="62807-119">Resource group name of the virtual machine scale set.</span></span>

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

### <span data-ttu-id="62807-120">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="62807-120">-VMScaleSetName</span></span>
<span data-ttu-id="62807-121">Sanal makine ölçek kümesi adı.</span><span class="sxs-lookup"><span data-stu-id="62807-121">The virtual machine scale set name.</span></span>

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

### <span data-ttu-id="62807-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62807-122">CommonParameters</span></span>
<span data-ttu-id="62807-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="62807-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62807-124">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="62807-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62807-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="62807-125">INPUTS</span></span>

### <span data-ttu-id="62807-126">System. String</span><span class="sxs-lookup"><span data-stu-id="62807-126">System.String</span></span>

## <span data-ttu-id="62807-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="62807-127">OUTPUTS</span></span>

### <span data-ttu-id="62807-128">Microsoft. Azure. Commands. COMPUTE. modeller. PSVmssVMDiskEncryptionStatusContext</span><span class="sxs-lookup"><span data-stu-id="62807-128">Microsoft.Azure.Commands.Compute.Models.PSVmssVMDiskEncryptionStatusContext</span></span>

## <span data-ttu-id="62807-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="62807-129">NOTES</span></span>

## <span data-ttu-id="62807-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="62807-130">RELATED LINKS</span></span>
