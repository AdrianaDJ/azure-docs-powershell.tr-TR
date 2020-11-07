---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 7B3259CD-079D-4E07-8608-F818522EE7CF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/start-azurermvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Start-AzureRmVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Start-AzureRmVM.md
ms.openlocfilehash: 121d9353baaa10058e101d3f8a7d398f345052ff
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763884"
---
# <span data-ttu-id="9cd5f-101">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="9cd5f-101">Start-AzureRmVM</span></span>

## <span data-ttu-id="9cd5f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9cd5f-102">SYNOPSIS</span></span>
<span data-ttu-id="9cd5f-103">Azure sanal makinesini başlatır.</span><span class="sxs-lookup"><span data-stu-id="9cd5f-103">Starts an Azure virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9cd5f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9cd5f-104">SYNTAX</span></span>

### <span data-ttu-id="9cd5f-105">ResourceGroupNameParameterSetName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="9cd5f-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Start-AzureRmVM [-Name] <String> [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9cd5f-106">Idparametersetname</span><span class="sxs-lookup"><span data-stu-id="9cd5f-106">IdParameterSetName</span></span>
```
Start-AzureRmVM [-Name] <String> [-Id] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9cd5f-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="9cd5f-107">DESCRIPTION</span></span>
<span data-ttu-id="9cd5f-108">**Start-AzureRmVM** cmdlet 'ı bir Azure sanal makinesini başlatır.</span><span class="sxs-lookup"><span data-stu-id="9cd5f-108">The **Start-AzureRmVM** cmdlet starts an Azure virtual machine.</span></span>

## <span data-ttu-id="9cd5f-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9cd5f-109">EXAMPLES</span></span>

### <span data-ttu-id="9cd5f-110">Örnek 1: sanal makine başlatma</span><span class="sxs-lookup"><span data-stu-id="9cd5f-110">Example 1: Start a virtual machine</span></span>
```
PS C:\> Start-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="9cd5f-111">Bu komut, ResourceGroup11 'da VirtualMachine07 adındaki sanal makineyi başlatır.</span><span class="sxs-lookup"><span data-stu-id="9cd5f-111">This command starts the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="9cd5f-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9cd5f-112">PARAMETERS</span></span>

### <span data-ttu-id="9cd5f-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="9cd5f-113">-AsJob</span></span>
<span data-ttu-id="9cd5f-114">Arka planda cmdlet 'i çalıştırın ve ilerlemeyi izlemek için bir Iş dönün.</span><span class="sxs-lookup"><span data-stu-id="9cd5f-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="9cd5f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9cd5f-115">-DefaultProfile</span></span>
<span data-ttu-id="9cd5f-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9cd5f-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9cd5f-117">-ID</span><span class="sxs-lookup"><span data-stu-id="9cd5f-117">-Id</span></span>
<span data-ttu-id="9cd5f-118">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="9cd5f-118">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9cd5f-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="9cd5f-119">-Name</span></span>
<span data-ttu-id="9cd5f-120">Sanal makine adı.</span><span class="sxs-lookup"><span data-stu-id="9cd5f-120">The virtual machine name.</span></span>

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

### <span data-ttu-id="9cd5f-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9cd5f-121">-ResourceGroupName</span></span>
<span data-ttu-id="9cd5f-122">Sanal makinenin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9cd5f-122">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9cd5f-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="9cd5f-123">-Confirm</span></span>
<span data-ttu-id="9cd5f-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="9cd5f-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9cd5f-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9cd5f-125">-WhatIf</span></span>
<span data-ttu-id="9cd5f-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="9cd5f-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9cd5f-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="9cd5f-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9cd5f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9cd5f-128">CommonParameters</span></span>
<span data-ttu-id="9cd5f-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9cd5f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9cd5f-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9cd5f-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9cd5f-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9cd5f-131">INPUTS</span></span>

### <span data-ttu-id="9cd5f-132">System. String</span><span class="sxs-lookup"><span data-stu-id="9cd5f-132">System.String</span></span>

## <span data-ttu-id="9cd5f-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9cd5f-133">OUTPUTS</span></span>

### <span data-ttu-id="9cd5f-134">Microsoft. Azure. Commands. COMPUTE. modeller. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="9cd5f-134">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="9cd5f-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9cd5f-135">NOTES</span></span>

## <span data-ttu-id="9cd5f-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9cd5f-136">RELATED LINKS</span></span>

[<span data-ttu-id="9cd5f-137">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="9cd5f-137">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="9cd5f-138">Yeni-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="9cd5f-138">New-AzureRmVM</span></span>](./New-AzureRmVM.md)

[<span data-ttu-id="9cd5f-139">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="9cd5f-139">Remove-AzureRmVM</span></span>](./Remove-AzureRmVM.md)

[<span data-ttu-id="9cd5f-140">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="9cd5f-140">Restart-AzureRmVM</span></span>](./Restart-AzureRmVM.md)

[<span data-ttu-id="9cd5f-141">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="9cd5f-141">Stop-AzureRmVM</span></span>](./Stop-AzureRmVM.md)

[<span data-ttu-id="9cd5f-142">Güncelleştirme-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="9cd5f-142">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


