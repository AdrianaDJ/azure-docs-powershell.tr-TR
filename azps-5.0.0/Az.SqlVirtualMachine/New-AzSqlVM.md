---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/new-azsqlvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzSqlVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzSqlVM.md
ms.openlocfilehash: 764312c64ae9887a6ef4243cc20b04535afcf81f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94276950"
---
# <span data-ttu-id="e3299-101">New-AzSqlVM</span><span class="sxs-lookup"><span data-stu-id="e3299-101">New-AzSqlVM</span></span>

## <span data-ttu-id="e3299-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e3299-102">SYNOPSIS</span></span>
<span data-ttu-id="e3299-103">Yeni bir SQL sanal makinesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e3299-103">Creates a new sql virtual machine.</span></span>

## <span data-ttu-id="e3299-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e3299-104">SYNTAX</span></span>

### <span data-ttu-id="e3299-105">NameParamaterList (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e3299-105">NameParamaterList (Default)</span></span>
```
New-AzSqlVM [-ResourceGroupName] <String> [-Name] <String> [-LicenseType] <String> -Location <String> [-AsJob]
 [-Offer <String>] [-Sku <String>] [-SqlManagementType <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3299-106">NameInputObject</span><span class="sxs-lookup"><span data-stu-id="e3299-106">NameInputObject</span></span>
```
New-AzSqlVM [-ResourceGroupName] <String> [-Name] <String> [-SqlVM] <AzureSqlVMModel> -Location <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e3299-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="e3299-107">DESCRIPTION</span></span>
<span data-ttu-id="e3299-108">New-AzSqlVM cmdlet 'i bir Azure SQL sanal makinesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e3299-108">The New-AzSqlVM cmdlet creates an Azure SQL virtual machine.</span></span>

## <span data-ttu-id="e3299-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e3299-109">EXAMPLES</span></span>

### <span data-ttu-id="e3299-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="e3299-110">Example 1</span></span>
```powershell
PS C:\> New-AzSqlVM  New-AzSqlVM -ResourceGroupName ResourceGroup01 -Name vm -LicenseType 'PAYG' -Sku Developer
Name ResourceGroupName  LicenseType Sku       Offer          SqlManagementType
---- -----------------  ----------- ---       -----          -----------------
vm   ResourceGroup01    PAYG        Developer SQL2017-WS2016 Full
```

<span data-ttu-id="e3299-111">Kaynak grubunda ad VM 'si olan yeni bir Azure SQL sanal makinesi oluşturur ResourceGroup01</span><span class="sxs-lookup"><span data-stu-id="e3299-111">Creates a new Azure SQL virtual machine with name vm in the resource group ResourceGroup01</span></span> 

## <span data-ttu-id="e3299-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e3299-112">PARAMETERS</span></span>

### <span data-ttu-id="e3299-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="e3299-113">-AsJob</span></span>
<span data-ttu-id="e3299-114">Arka planda cmdlet 'i çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="e3299-114">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="e3299-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3299-115">-DefaultProfile</span></span>
<span data-ttu-id="e3299-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e3299-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e3299-117">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="e3299-117">-LicenseType</span></span>
<span data-ttu-id="e3299-118">SQL sanal makine lisans türü.</span><span class="sxs-lookup"><span data-stu-id="e3299-118">SQL virtual machine license type.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParamaterList
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3299-119">-Konum</span><span class="sxs-lookup"><span data-stu-id="e3299-119">-Location</span></span>
<span data-ttu-id="e3299-120">SQL sanal makine konumu.</span><span class="sxs-lookup"><span data-stu-id="e3299-120">SQL virtual machine location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3299-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="e3299-121">-Name</span></span>
<span data-ttu-id="e3299-122">SQL sanal makine adı.</span><span class="sxs-lookup"><span data-stu-id="e3299-122">SQL virtual machine name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SqlVMName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3299-123">-Teklif</span><span class="sxs-lookup"><span data-stu-id="e3299-123">-Offer</span></span>
<span data-ttu-id="e3299-124">SQL sanal makinesi teklifi.</span><span class="sxs-lookup"><span data-stu-id="e3299-124">SQL virtual machine offer.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParamaterList
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3299-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3299-125">-ResourceGroupName</span></span>
<span data-ttu-id="e3299-126">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="e3299-126">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3299-127">-SKU</span><span class="sxs-lookup"><span data-stu-id="e3299-127">-Sku</span></span>
<span data-ttu-id="e3299-128">SQL sanal makinesi sürümü türü.</span><span class="sxs-lookup"><span data-stu-id="e3299-128">SQL virtual machine edition type.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParamaterList
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3299-129">-SqlManagementType</span><span class="sxs-lookup"><span data-stu-id="e3299-129">-SqlManagementType</span></span>
<span data-ttu-id="e3299-130">SQL sanal makine yönetimi türü.</span><span class="sxs-lookup"><span data-stu-id="e3299-130">SQL virtual machine management type.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParamaterList
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3299-131">-SqlVM</span><span class="sxs-lookup"><span data-stu-id="e3299-131">-SqlVM</span></span>
<span data-ttu-id="e3299-132">SQL sanal makinesi nesnesi.</span><span class="sxs-lookup"><span data-stu-id="e3299-132">SQL virtual machine object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel
Parameter Sets: NameInputObject
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e3299-133">Etiketli</span><span class="sxs-lookup"><span data-stu-id="e3299-133">-Tag</span></span>
<span data-ttu-id="e3299-134">SQL sanal makinesiyle ilişkilendirilecek Etiketler</span><span class="sxs-lookup"><span data-stu-id="e3299-134">The tags to associate with the SQL virtual machine</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: NameParamaterList
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3299-135">-Onay</span><span class="sxs-lookup"><span data-stu-id="e3299-135">-Confirm</span></span>
<span data-ttu-id="e3299-136">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e3299-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e3299-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3299-137">-WhatIf</span></span>
<span data-ttu-id="e3299-138">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e3299-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e3299-139">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e3299-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e3299-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3299-140">CommonParameters</span></span>
<span data-ttu-id="e3299-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e3299-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3299-142">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="e3299-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3299-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e3299-143">INPUTS</span></span>

### <span data-ttu-id="e3299-144">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. model. azures, Vmmodel</span><span class="sxs-lookup"><span data-stu-id="e3299-144">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="e3299-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e3299-145">OUTPUTS</span></span>

### <span data-ttu-id="e3299-146">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. model. azures, Vmmodel</span><span class="sxs-lookup"><span data-stu-id="e3299-146">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="e3299-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e3299-147">NOTES</span></span>

## <span data-ttu-id="e3299-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e3299-148">RELATED LINKS</span></span>
