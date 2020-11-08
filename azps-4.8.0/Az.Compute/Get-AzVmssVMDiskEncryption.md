---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmssvmdiskencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssVMDiskEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssVMDiskEncryption.md
ms.openlocfilehash: 8ff3ad92f976e6a8af9c4a24e143ed3859832d35
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94266665"
---
# <span data-ttu-id="e9db0-101">Get-AzVmssVMDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="e9db0-101">Get-AzVmssVMDiskEncryption</span></span>

## <span data-ttu-id="e9db0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e9db0-102">SYNOPSIS</span></span>
<span data-ttu-id="e9db0-103">VM Ölçek kümesindeki VM 'lerin disk şifreleme durumunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="e9db0-103">Shows the disk encryption status of VMs in a VM scale set.</span></span>

## <span data-ttu-id="e9db0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e9db0-104">SYNTAX</span></span>

```
Get-AzVmssVMDiskEncryption [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String>]
 [-ExtensionName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e9db0-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e9db0-105">DESCRIPTION</span></span>
<span data-ttu-id="e9db0-106">VM Ölçek kümesinin disk şifreleme durumunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="e9db0-106">Shows the disk encryption status of VM scale set.</span></span>

## <span data-ttu-id="e9db0-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e9db0-107">EXAMPLES</span></span>

### <span data-ttu-id="e9db0-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="e9db0-108">Example 1</span></span>
```
PS C:\> Get-AzVmssVMDiskEncryption -ResourceGroupName "Group001" -VMScaleSetName "VMSS001" -InstanceId "1"
```

<span data-ttu-id="e9db0-109">Group001 adındaki kaynak grubuna ait VMSS001 adındaki VM Ölçek kümesindeki VM örneğinin disk şifreleme durumunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="e9db0-109">Shows the disk encryption status of VM instance 1 in the VM scale set named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="e9db0-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e9db0-110">PARAMETERS</span></span>

### <span data-ttu-id="e9db0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9db0-111">-DefaultProfile</span></span>
<span data-ttu-id="e9db0-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e9db0-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e9db0-113">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="e9db0-113">-ExtensionName</span></span>
<span data-ttu-id="e9db0-114">Uzantı adı.</span><span class="sxs-lookup"><span data-stu-id="e9db0-114">The extension name.</span></span>
<span data-ttu-id="e9db0-115">Bu parametre belirtilmezse, kullanılan varsayılan değerler Windows VM 'ler için AzureDiskEncryption ve Linux VM 'Ler için AzureDiskEncryptionForLinux.</span><span class="sxs-lookup"><span data-stu-id="e9db0-115">If this parameter is not specified, default values used are AzureDiskEncryption for windows VMs and AzureDiskEncryptionForLinux for Linux VMs.</span></span>

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

### <span data-ttu-id="e9db0-116">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="e9db0-116">-InstanceId</span></span>
<span data-ttu-id="e9db0-117">Örnek KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="e9db0-117">Specifies the instance ID.</span></span>

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

### <span data-ttu-id="e9db0-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e9db0-118">-ResourceGroupName</span></span>
<span data-ttu-id="e9db0-119">Sanal makine ölçek kümesinin kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="e9db0-119">Resource group name of the virtual machine scale set.</span></span>

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

### <span data-ttu-id="e9db0-120">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="e9db0-120">-VMScaleSetName</span></span>
<span data-ttu-id="e9db0-121">Sanal makine ölçek kümesi adı.</span><span class="sxs-lookup"><span data-stu-id="e9db0-121">The virtual machine scale set name.</span></span>

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

### <span data-ttu-id="e9db0-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9db0-122">CommonParameters</span></span>
<span data-ttu-id="e9db0-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e9db0-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9db0-124">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="e9db0-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9db0-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e9db0-125">INPUTS</span></span>

### <span data-ttu-id="e9db0-126">System. String</span><span class="sxs-lookup"><span data-stu-id="e9db0-126">System.String</span></span>

## <span data-ttu-id="e9db0-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e9db0-127">OUTPUTS</span></span>

### <span data-ttu-id="e9db0-128">Microsoft. Azure. Commands. COMPUTE. modeller. PSVmssVMDiskEncryptionStatusContext</span><span class="sxs-lookup"><span data-stu-id="e9db0-128">Microsoft.Azure.Commands.Compute.Models.PSVmssVMDiskEncryptionStatusContext</span></span>

## <span data-ttu-id="e9db0-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e9db0-129">NOTES</span></span>

## <span data-ttu-id="e9db0-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e9db0-130">RELATED LINKS</span></span>
