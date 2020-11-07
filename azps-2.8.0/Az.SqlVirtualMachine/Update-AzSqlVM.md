---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/update-azsqlvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Update-AzSqlVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Update-AzSqlVM.md
ms.openlocfilehash: bfc64aeb344e9913bf72ae7b51559bb613209994
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93933959"
---
# <span data-ttu-id="3d8a6-101">Update-AzSqlVM</span><span class="sxs-lookup"><span data-stu-id="3d8a6-101">Update-AzSqlVM</span></span>

## <span data-ttu-id="3d8a6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3d8a6-102">SYNOPSIS</span></span>
<span data-ttu-id="3d8a6-103">SQL sanal makinesini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="3d8a6-103">Updates a sql virtual machine.</span></span>

## <span data-ttu-id="3d8a6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3d8a6-104">SYNTAX</span></span>

### <span data-ttu-id="3d8a6-105">NameParamaterList (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="3d8a6-105">NameParamaterList (Default)</span></span>
```
Update-AzSqlVM [-ResourceGroupName] <String> [-Name] <String> [-LicenseType <String>] [-Offer <String>]
 [-Sku <String>] [-SqlManagementType <String>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3d8a6-106">NameInputObject</span><span class="sxs-lookup"><span data-stu-id="3d8a6-106">NameInputObject</span></span>
```
Update-AzSqlVM [-ResourceGroupName] <String> [-Name] <String> [-InputObject] <AzureSqlVMModel> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3d8a6-107">ResourceIdParamaterList</span><span class="sxs-lookup"><span data-stu-id="3d8a6-107">ResourceIdParamaterList</span></span>
```
Update-AzSqlVM [-LicenseType <String>] [-Offer <String>] [-Sku <String>] [-SqlManagementType <String>]
 [-Tag <Hashtable>] [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3d8a6-108">Kaynakıdınputobject</span><span class="sxs-lookup"><span data-stu-id="3d8a6-108">ResourceIdInputObject</span></span>
```
Update-AzSqlVM [-InputObject] <AzureSqlVMModel> [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3d8a6-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="3d8a6-109">DESCRIPTION</span></span>
<span data-ttu-id="3d8a6-110">Update-AzSqlVM cmdlet bir SQL sanal makinesini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="3d8a6-110">The Update-AzSqlVM cmdlet updates a sql virtual machine.</span></span>

## <span data-ttu-id="3d8a6-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3d8a6-111">EXAMPLES</span></span>

### <span data-ttu-id="3d8a6-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="3d8a6-112">Example 1</span></span>
```powershell
PS C:\> $tags = @{'key'='value'}
PS C:\> $vm = Update-AzSqlVM -InputObject $vm -Tags $tags
PS C:\> $group.Tags
Name                           Value
----                           -----
key                            value
```

<span data-ttu-id="3d8a6-113">SQL sanal makinesinin etiketlerini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="3d8a6-113">Updates the tags of a sql virtual machine.</span></span>

## <span data-ttu-id="3d8a6-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3d8a6-114">PARAMETERS</span></span>

### <span data-ttu-id="3d8a6-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="3d8a6-115">-AsJob</span></span>
<span data-ttu-id="3d8a6-116">Arka planda cmdlet 'i çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="3d8a6-116">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="3d8a6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d8a6-117">-DefaultProfile</span></span>
<span data-ttu-id="3d8a6-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3d8a6-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3d8a6-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3d8a6-119">-InputObject</span></span>
<span data-ttu-id="3d8a6-120">SQL sanal makinesi nesnesi.</span><span class="sxs-lookup"><span data-stu-id="3d8a6-120">SQL virtual machine object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel
Parameter Sets: NameInputObject, ResourceIdInputObject
Aliases: SqlVM

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3d8a6-121">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="3d8a6-121">-LicenseType</span></span>
<span data-ttu-id="3d8a6-122">SQL sanal makine lisans türü.</span><span class="sxs-lookup"><span data-stu-id="3d8a6-122">SQL virtual machine license type.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParamaterList, ResourceIdParamaterList
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d8a6-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="3d8a6-123">-Name</span></span>
<span data-ttu-id="3d8a6-124">SQL sanal makine adı.</span><span class="sxs-lookup"><span data-stu-id="3d8a6-124">SQL virtual machine name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParamaterList, NameInputObject
Aliases: SqlVMName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d8a6-125">-Teklif</span><span class="sxs-lookup"><span data-stu-id="3d8a6-125">-Offer</span></span>
<span data-ttu-id="3d8a6-126">SQL sanal makinesi teklifi.</span><span class="sxs-lookup"><span data-stu-id="3d8a6-126">SQL virtual machine offer.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParamaterList, ResourceIdParamaterList
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d8a6-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d8a6-127">-ResourceGroupName</span></span>
<span data-ttu-id="3d8a6-128">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="3d8a6-128">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParamaterList, NameInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d8a6-129">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="3d8a6-129">-ResourceId</span></span>
<span data-ttu-id="3d8a6-130">SQL sanal makinesi kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="3d8a6-130">SQL virtual machine resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParamaterList, ResourceIdInputObject
Aliases: SqlVMId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d8a6-131">-SKU</span><span class="sxs-lookup"><span data-stu-id="3d8a6-131">-Sku</span></span>
<span data-ttu-id="3d8a6-132">SQL sanal makinesi sürümü türü.</span><span class="sxs-lookup"><span data-stu-id="3d8a6-132">SQL virtual machine edition type.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParamaterList, ResourceIdParamaterList
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d8a6-133">-SqlManagementType</span><span class="sxs-lookup"><span data-stu-id="3d8a6-133">-SqlManagementType</span></span>
<span data-ttu-id="3d8a6-134">SQL sanal makine yönetimi türü.</span><span class="sxs-lookup"><span data-stu-id="3d8a6-134">SQL virtual machine management type.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParamaterList, ResourceIdParamaterList
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d8a6-135">Etiketli</span><span class="sxs-lookup"><span data-stu-id="3d8a6-135">-Tag</span></span>
<span data-ttu-id="3d8a6-136">SQL sanal makinesiyle ilişkilendirilecek Etiketler</span><span class="sxs-lookup"><span data-stu-id="3d8a6-136">The tags to associate with the SQL virtual machine</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: NameParamaterList, ResourceIdParamaterList
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d8a6-137">-Onay</span><span class="sxs-lookup"><span data-stu-id="3d8a6-137">-Confirm</span></span>
<span data-ttu-id="3d8a6-138">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="3d8a6-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3d8a6-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d8a6-139">-WhatIf</span></span>
<span data-ttu-id="3d8a6-140">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3d8a6-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3d8a6-141">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="3d8a6-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3d8a6-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d8a6-142">CommonParameters</span></span>
<span data-ttu-id="3d8a6-143">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3d8a6-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d8a6-144">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="3d8a6-144">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d8a6-145">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3d8a6-145">INPUTS</span></span>

### <span data-ttu-id="3d8a6-146">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. model. azures, Vmmodel</span><span class="sxs-lookup"><span data-stu-id="3d8a6-146">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="3d8a6-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3d8a6-147">OUTPUTS</span></span>

### <span data-ttu-id="3d8a6-148">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. model. azures, Vmmodel</span><span class="sxs-lookup"><span data-stu-id="3d8a6-148">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="3d8a6-149">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3d8a6-149">NOTES</span></span>

## <span data-ttu-id="3d8a6-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3d8a6-150">RELATED LINKS</span></span>
