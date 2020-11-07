---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmssdiskencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssDiskEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssDiskEncryption.md
ms.openlocfilehash: 5219b43a1d80515f0bce02c5f6fdd2117b736a00
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93761332"
---
# <span data-ttu-id="c2193-101">Get-AzVmssDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="c2193-101">Get-AzVmssDiskEncryption</span></span>

## <span data-ttu-id="c2193-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c2193-102">SYNOPSIS</span></span>
<span data-ttu-id="c2193-103">VM Ölçek kümesinin disk şifreleme durumunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="c2193-103">Shows the disk encryption status of a VM scale set.</span></span>

## <span data-ttu-id="c2193-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c2193-104">SYNTAX</span></span>

```
Get-AzVmssDiskEncryption [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>]
 [[-ExtensionName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c2193-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c2193-105">DESCRIPTION</span></span>
<span data-ttu-id="c2193-106">VM Ölçek kümesinin disk şifreleme durumunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="c2193-106">Shows the disk encryption status of a VM scale set.</span></span>

## <span data-ttu-id="c2193-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c2193-107">EXAMPLES</span></span>

### <span data-ttu-id="c2193-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="c2193-108">Example 1</span></span>
```
PS C:\> Get-AzVmssDiskEncryption -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="c2193-109">Group001 adındaki kaynak grubuna ait olan VMSS001 adındaki VM Ölçek kümesinin disk şifreleme durumunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="c2193-109">Shows the disk encryption status of the VM scale set named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="c2193-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c2193-110">PARAMETERS</span></span>

### <span data-ttu-id="c2193-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2193-111">-DefaultProfile</span></span>
<span data-ttu-id="c2193-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c2193-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c2193-113">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="c2193-113">-ExtensionName</span></span>
<span data-ttu-id="c2193-114">Uzantı adı.</span><span class="sxs-lookup"><span data-stu-id="c2193-114">The extension name.</span></span>
<span data-ttu-id="c2193-115">Bu parametre belirtilmezse, kullanılan varsayılan değerler Windows VM 'ler için AzureDiskEncryption ve Linux VM 'Ler için AzureDiskEncryptionForLinux.</span><span class="sxs-lookup"><span data-stu-id="c2193-115">If this parameter is not specified, default values used are AzureDiskEncryption for windows VMs and AzureDiskEncryptionForLinux for Linux VMs.</span></span>

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

### <span data-ttu-id="c2193-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2193-116">-ResourceGroupName</span></span>
<span data-ttu-id="c2193-117">Sanal makine ölçek kümesinin kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="c2193-117">Resource group name of the virtual machine scale set</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2193-118">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="c2193-118">-VMScaleSetName</span></span>
<span data-ttu-id="c2193-119">Sanal makine ölçek kümesi adı.</span><span class="sxs-lookup"><span data-stu-id="c2193-119">The virtual machine scale set name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2193-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2193-120">CommonParameters</span></span>
<span data-ttu-id="c2193-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c2193-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2193-122">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="c2193-122">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2193-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c2193-123">INPUTS</span></span>

### <span data-ttu-id="c2193-124">System. String</span><span class="sxs-lookup"><span data-stu-id="c2193-124">System.String</span></span>

## <span data-ttu-id="c2193-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c2193-125">OUTPUTS</span></span>

### <span data-ttu-id="c2193-126">Microsoft. Azure. Commands. COMPUTE. modeller. PSVmssDiskEncryptionStatusContext</span><span class="sxs-lookup"><span data-stu-id="c2193-126">Microsoft.Azure.Commands.Compute.Models.PSVmssDiskEncryptionStatusContext</span></span>

## <span data-ttu-id="c2193-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c2193-127">NOTES</span></span>

## <span data-ttu-id="c2193-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c2193-128">RELATED LINKS</span></span>
