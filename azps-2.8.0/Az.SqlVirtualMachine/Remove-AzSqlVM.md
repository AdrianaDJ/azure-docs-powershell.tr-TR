---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/remove-azsqlvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Remove-AzSqlVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Remove-AzSqlVM.md
ms.openlocfilehash: 5a9d08e007e951700ef6e78fd211303e17d0351c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93933965"
---
# <span data-ttu-id="1c076-101">Remove-AzSqlVM</span><span class="sxs-lookup"><span data-stu-id="1c076-101">Remove-AzSqlVM</span></span>

## <span data-ttu-id="1c076-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1c076-102">SYNOPSIS</span></span>
<span data-ttu-id="1c076-103">SQL sanal makinesini siler.</span><span class="sxs-lookup"><span data-stu-id="1c076-103">Deletes a sql virtual machine.</span></span>

## <span data-ttu-id="1c076-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1c076-104">SYNTAX</span></span>

### <span data-ttu-id="1c076-105">Ad (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="1c076-105">Name (Default)</span></span>
```
Remove-AzSqlVM [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1c076-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="1c076-106">InputObject</span></span>
```
Remove-AzSqlVM [-InputObject] <AzureSqlVMModel> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1c076-107">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="1c076-107">ResourceId</span></span>
```
Remove-AzSqlVM [-ResourceId] <String> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1c076-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="1c076-108">DESCRIPTION</span></span>
<span data-ttu-id="1c076-109">Remove-AzSqlVM cmdlet bir SQL sanal makinesini siler.</span><span class="sxs-lookup"><span data-stu-id="1c076-109">The Remove-AzSqlVM cmdlet deletes a sql virtual machine.</span></span>

## <span data-ttu-id="1c076-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1c076-110">EXAMPLES</span></span>

### <span data-ttu-id="1c076-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="1c076-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSqlVM -ResourceGroupName "ResourceGroup01" -Name "vm"
```

<span data-ttu-id="1c076-112">Kaynak grubundaki ResourceGroup01 Azure SQL sanal makinesini siler.</span><span class="sxs-lookup"><span data-stu-id="1c076-112">Deletes the Azure SQL virtual machine "vm" in the resource group ResourceGroup01.</span></span>

## <span data-ttu-id="1c076-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1c076-113">PARAMETERS</span></span>

### <span data-ttu-id="1c076-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="1c076-114">-AsJob</span></span>
<span data-ttu-id="1c076-115">Arka planda cmdlet 'i çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="1c076-115">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="1c076-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c076-116">-DefaultProfile</span></span>
<span data-ttu-id="1c076-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1c076-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1c076-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1c076-118">-InputObject</span></span>
<span data-ttu-id="1c076-119">SQL sanal makinesi nesnesi.</span><span class="sxs-lookup"><span data-stu-id="1c076-119">SQL virtual machine object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel
Parameter Sets: InputObject
Aliases: SqlVM

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1c076-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="1c076-120">-Name</span></span>
<span data-ttu-id="1c076-121">SQL sanal makine adı.</span><span class="sxs-lookup"><span data-stu-id="1c076-121">SQL virtual machine name.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases: SqlVMName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c076-122">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="1c076-122">-PassThru</span></span>
<span data-ttu-id="1c076-123">, Cmdlet 'in yürütülmesinin sonunda silinen kaynağın çıktısının mi edilmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1c076-123">Specifies whether to output the deleted resource at end of cmdlet execution.</span></span>

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

### <span data-ttu-id="1c076-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c076-124">-ResourceGroupName</span></span>
<span data-ttu-id="1c076-125">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="1c076-125">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c076-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="1c076-126">-ResourceId</span></span>
<span data-ttu-id="1c076-127">SQL sanal makinesi kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="1c076-127">SQL virtual machine resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases: SqlVMId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c076-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="1c076-128">-Confirm</span></span>
<span data-ttu-id="1c076-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="1c076-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1c076-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1c076-130">-WhatIf</span></span>
<span data-ttu-id="1c076-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1c076-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1c076-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="1c076-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1c076-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c076-133">CommonParameters</span></span>
<span data-ttu-id="1c076-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1c076-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c076-135">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="1c076-135">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c076-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1c076-136">INPUTS</span></span>

### <span data-ttu-id="1c076-137">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. model. azures, Vmmodel</span><span class="sxs-lookup"><span data-stu-id="1c076-137">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="1c076-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1c076-138">OUTPUTS</span></span>

### <span data-ttu-id="1c076-139">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. model. azures, Vmmodel</span><span class="sxs-lookup"><span data-stu-id="1c076-139">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="1c076-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1c076-140">NOTES</span></span>

## <span data-ttu-id="1c076-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1c076-141">RELATED LINKS</span></span>
