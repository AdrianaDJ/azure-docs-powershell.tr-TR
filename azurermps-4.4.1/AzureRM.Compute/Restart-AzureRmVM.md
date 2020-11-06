---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: EF155949-5766-4BC4-9C8A-2B97E8EA032D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Restart-AzureRmVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Restart-AzureRmVM.md
ms.openlocfilehash: 5a848c2e4a13df6a38c67e067531ff8581bd595e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586952"
---
# <span data-ttu-id="93204-101">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="93204-101">Restart-AzureRmVM</span></span>

## <span data-ttu-id="93204-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="93204-102">SYNOPSIS</span></span>
<span data-ttu-id="93204-103">Azure sanal makinesini yeniden başlatır.</span><span class="sxs-lookup"><span data-stu-id="93204-103">Restarts an Azure virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="93204-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="93204-104">SYNTAX</span></span>

### <span data-ttu-id="93204-105">RestartResourceGroupNameParameterSetName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="93204-105">RestartResourceGroupNameParameterSetName (Default)</span></span>
```
Restart-AzureRmVM [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="93204-106">PerformMaintenanceResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="93204-106">PerformMaintenanceResourceGroupNameParameterSetName</span></span>
```
Restart-AzureRmVM [-ResourceGroupName] <String> [-Name] <String> [-PerformMaintenance]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="93204-107">Restartivseçparametersetname</span><span class="sxs-lookup"><span data-stu-id="93204-107">RestartIdParameterSetName</span></span>
```
Restart-AzureRmVM [-Id] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="93204-108">PerformMaintenanceIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="93204-108">PerformMaintenanceIdParameterSetName</span></span>
```
Restart-AzureRmVM [-Id] <String> [-Name] <String> [-PerformMaintenance]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="93204-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="93204-109">DESCRIPTION</span></span>
<span data-ttu-id="93204-110">**Restart-AzureRmVM** cmdlet 'ı bir Azure sanal makinesini yeniden başlatır.</span><span class="sxs-lookup"><span data-stu-id="93204-110">The **Restart-AzureRmVM** cmdlet restarts an Azure virtual machine.</span></span>

## <span data-ttu-id="93204-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="93204-111">EXAMPLES</span></span>

### <span data-ttu-id="93204-112">Örnek 1: sanal makineyi yeniden başlatın</span><span class="sxs-lookup"><span data-stu-id="93204-112">Example 1: Restart a virtual machine</span></span>
```
PS C:\> Restart-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="93204-113">Bu komut, ResourceGroup11 'da VirtualMachine07 adındaki sanal makineyi yeniden başlatır.</span><span class="sxs-lookup"><span data-stu-id="93204-113">This command restarts the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="93204-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="93204-114">PARAMETERS</span></span>

### <span data-ttu-id="93204-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93204-115">-DefaultProfile</span></span>
<span data-ttu-id="93204-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="93204-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="93204-117">-ID</span><span class="sxs-lookup"><span data-stu-id="93204-117">-Id</span></span>
<span data-ttu-id="93204-118">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="93204-118">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: RestartIdParameterSetName, PerformMaintenanceIdParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93204-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="93204-119">-Name</span></span>
<span data-ttu-id="93204-120">Sanal makine adı.</span><span class="sxs-lookup"><span data-stu-id="93204-120">The virtual machine name.</span></span>

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

### <span data-ttu-id="93204-121">-PerformMaintenance</span><span class="sxs-lookup"><span data-stu-id="93204-121">-PerformMaintenance</span></span>
<span data-ttu-id="93204-122">Sanal makinenin bakımını yapmak için.</span><span class="sxs-lookup"><span data-stu-id="93204-122">To perform the maintenance of virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: PerformMaintenanceResourceGroupNameParameterSetName, PerformMaintenanceIdParameterSetName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93204-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93204-123">-ResourceGroupName</span></span>
<span data-ttu-id="93204-124">Sanal makinenin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="93204-124">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: RestartResourceGroupNameParameterSetName, PerformMaintenanceResourceGroupNameParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93204-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="93204-125">-Confirm</span></span>
<span data-ttu-id="93204-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="93204-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="93204-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="93204-127">-WhatIf</span></span>
<span data-ttu-id="93204-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="93204-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="93204-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="93204-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="93204-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93204-130">CommonParameters</span></span>
<span data-ttu-id="93204-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="93204-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93204-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93204-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93204-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="93204-133">INPUTS</span></span>

## <span data-ttu-id="93204-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="93204-134">OUTPUTS</span></span>

## <span data-ttu-id="93204-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="93204-135">NOTES</span></span>

## <span data-ttu-id="93204-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="93204-136">RELATED LINKS</span></span>

[<span data-ttu-id="93204-137">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="93204-137">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="93204-138">Yeni-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="93204-138">New-AzureRmVM</span></span>](./New-AzureRmVM.md)

[<span data-ttu-id="93204-139">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="93204-139">Remove-AzureRmVM</span></span>](./Remove-AzureRmVM.md)

[<span data-ttu-id="93204-140">Başlangıç-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="93204-140">Start-AzureRmVM</span></span>](./Start-AzureRmVM.md)

[<span data-ttu-id="93204-141">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="93204-141">Stop-AzureRmVM</span></span>](./Stop-AzureRmVM.md)

[<span data-ttu-id="93204-142">Güncelleştirme-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="93204-142">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


