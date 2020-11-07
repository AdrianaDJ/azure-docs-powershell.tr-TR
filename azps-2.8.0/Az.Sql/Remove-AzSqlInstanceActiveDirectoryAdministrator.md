---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlinstanceactivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceActiveDirectoryAdministrator.md
ms.openlocfilehash: fc2a5b4c25804658ad30c5f3554688746bdde74a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93933802"
---
# <span data-ttu-id="67ded-101">Remove-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="67ded-101">Remove-AzSqlInstanceActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="67ded-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="67ded-102">SYNOPSIS</span></span>
<span data-ttu-id="67ded-103">SQL yönetilen örneği için Azure AD yöneticisi 'ni kaldırır.</span><span class="sxs-lookup"><span data-stu-id="67ded-103">Removes an Azure AD administrator for SQL Managed Instance.</span></span>

## <span data-ttu-id="67ded-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="67ded-104">SYNTAX</span></span>

### <span data-ttu-id="67ded-105">Useresourcegroupandınstancenameparameterset (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="67ded-105">UseResourceGroupAndInstanceNameParameterSet (Default)</span></span>
```
Remove-AzSqlInstanceActiveDirectoryAdministrator [-Force] [-PassThru] [-ResourceGroupName] <String>
 [-InstanceName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="67ded-106">UseInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="67ded-106">UseInputObjectParameterSet</span></span>
```
Remove-AzSqlInstanceActiveDirectoryAdministrator [-Force] [-PassThru]
 [-InputObject <AzureSqlManagedInstanceModel>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="67ded-107">Userresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="67ded-107">UserResourceIdParameterSet</span></span>
```
Remove-AzSqlInstanceActiveDirectoryAdministrator [-Force] [-PassThru] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="67ded-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="67ded-108">DESCRIPTION</span></span>
<span data-ttu-id="67ded-109">**Remove-Azsqlınstanceactivedirectoryadministrator** cmdlet 'i, geçerli abonelikteki AzureSQL yönetilen örneği Için Azure Active Directory (Azure AD) yöneticisini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="67ded-109">The **Remove-AzSqlInstanceActiveDirectoryAdministrator** cmdlet removes an Azure Active Directory (Azure AD) administrator for AzureSQL Managed Instance in the current subscription.</span></span>

## <span data-ttu-id="67ded-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="67ded-110">EXAMPLES</span></span>

### <span data-ttu-id="67ded-111">Örnek 1: yöneticiyi kaldırma</span><span class="sxs-lookup"><span data-stu-id="67ded-111">Example 1: Remove an administrator</span></span>
```
PS C:\>Remove-AzSqlInstanceActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstanceName01" -Confirm -PassThru
Are you sure you want to remove the Azure Sql Instance Active Directory Administrator on managed instance 'ManagedInstanceName01'? 
[Y] Yes [A] Yes to All [N] No [L] No to All [S] Suspend [?] Help (default is "Y"): Y 

ResourceGroupName InstanceName          DisplayName ObjectId 
----------------- --------------------- ----------- -------- 
ResourceGroup01   ManagedInstanceName01 DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="67ded-112">Bu komut, kaynak grubuyla ilişkili ManagedInstanceName01 adlı yönetilen örnek için Azure AD yöneticisi 'ni kaldırır.</span><span class="sxs-lookup"><span data-stu-id="67ded-112">This command removes the Azure AD administrator for the managed instance named ManagedInstanceName01 associated with the resource group ResourceGroup01.</span></span>

### <span data-ttu-id="67ded-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="67ded-113">Example 2</span></span>
```powershell
PS C:\>Get-AzSqlInstance -ResourceGroupName "ResourceGroup01" -Name "ManagedInstance1" | Remove-AzSqlInstanceActiveDirectoryAdministrator -Confirm -PassThru
Are you sure you want to remove the Azure Sql Instance Active Directory Administrator on managed instance 'ManagedInstanceName01'? 
[Y] Yes [A] Yes to All [N] No [L] No to All [S] Suspend [?] Help (default is "Y"): Y 

ResourceGroupName InstanceName          DisplayName ObjectId 
----------------- --------------------- ----------- -------- 
ResourceGroup01   ManagedInstanceName01 DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="67ded-114">Bu komut, yönetilen örnek nesnesinden Azure AD yöneticisi 'ni kaldırır.</span><span class="sxs-lookup"><span data-stu-id="67ded-114">This command removes the Azure AD administrator from the managed instance object.</span></span>

### <span data-ttu-id="67ded-115">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="67ded-115">Example 3</span></span>
```powershell
PS C:\>Get-AzSqlInstance -ResourceId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Sql/managedInstances/ManagedInstance1" | Remove-AzSqlInstanceActiveDirectoryAdministrator -Confirm -PassThru
Are you sure you want to remove the Azure Sql Instance Active Directory Administrator on managed instance 'ManagedInstanceName01'? 
[Y] Yes [A] Yes to All [N] No [L] No to All [S] Suspend [?] Help (default is "Y"): Y 

ResourceGroupName InstanceName          DisplayName ObjectId 
----------------- --------------------- ----------- -------- 
ResourceGroup01   ManagedInstanceName01 DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="67ded-116">Bu komut, yönetilen örnek kaynak tanımlayıcısını kullanarak Azure AD yöneticisi 'ni kaldırır.</span><span class="sxs-lookup"><span data-stu-id="67ded-116">This command removes the Azure AD administrator using managed instance resource identifier.</span></span>

## <span data-ttu-id="67ded-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="67ded-117">PARAMETERS</span></span>

### <span data-ttu-id="67ded-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67ded-118">-DefaultProfile</span></span>
<span data-ttu-id="67ded-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="67ded-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="67ded-120">-Force</span><span class="sxs-lookup"><span data-stu-id="67ded-120">-Force</span></span>
<span data-ttu-id="67ded-121">Eylemi gerçekleştirmek için onay iletisini atla</span><span class="sxs-lookup"><span data-stu-id="67ded-121">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="67ded-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="67ded-122">-InputObject</span></span>
<span data-ttu-id="67ded-123">Kullanılacak yönetilen örnek nesnesi.</span><span class="sxs-lookup"><span data-stu-id="67ded-123">The managed instance object to use.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel
Parameter Sets: UseInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="67ded-124">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="67ded-124">-InstanceName</span></span>
<span data-ttu-id="67ded-125">SQL yönetilen örnek adı.</span><span class="sxs-lookup"><span data-stu-id="67ded-125">SQL Managed Instance name.</span></span>

```yaml
Type: System.String
Parameter Sets: UseResourceGroupAndInstanceNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67ded-126">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="67ded-126">-PassThru</span></span>
<span data-ttu-id="67ded-127">Kaldırılan AD yöneticisinin verilip verilmeyeceğini tanımlar</span><span class="sxs-lookup"><span data-stu-id="67ded-127">Defines whether to return the removed AD administrator</span></span>

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

### <span data-ttu-id="67ded-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67ded-128">-ResourceGroupName</span></span>
<span data-ttu-id="67ded-129">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="67ded-129">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: UseResourceGroupAndInstanceNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67ded-130">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="67ded-130">-ResourceId</span></span>
<span data-ttu-id="67ded-131">Kullanılacak örneğinin kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="67ded-131">The resource id of instance to use</span></span>

```yaml
Type: System.String
Parameter Sets: UserResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67ded-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="67ded-132">-Confirm</span></span>
<span data-ttu-id="67ded-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="67ded-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="67ded-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67ded-134">-WhatIf</span></span>
<span data-ttu-id="67ded-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="67ded-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="67ded-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="67ded-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="67ded-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67ded-137">CommonParameters</span></span>
<span data-ttu-id="67ded-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="67ded-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67ded-139">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="67ded-139">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67ded-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="67ded-140">INPUTS</span></span>

### <span data-ttu-id="67ded-141">System. String</span><span class="sxs-lookup"><span data-stu-id="67ded-141">System.String</span></span>

## <span data-ttu-id="67ded-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="67ded-142">OUTPUTS</span></span>

### <span data-ttu-id="67ded-143">Microsoft. Azure. Commands. Sql. ınstanceactivedirectoryadministrator. model. Azuresdınstanceactivedirectoryadministratormodel</span><span class="sxs-lookup"><span data-stu-id="67ded-143">Microsoft.Azure.Commands.Sql.InstanceActiveDirectoryAdministrator.Model.AzureSqlInstanceActiveDirectoryAdministratorModel</span></span>

## <span data-ttu-id="67ded-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="67ded-144">NOTES</span></span>

## <span data-ttu-id="67ded-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="67ded-145">RELATED LINKS</span></span>

[<span data-ttu-id="67ded-146">Set-Azsqlınstanceactivedirectoryadministrator</span><span class="sxs-lookup"><span data-stu-id="67ded-146">Set-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Set-AzSqlInstanceActiveDirectoryAdministrator.md)

[<span data-ttu-id="67ded-147">Get-Azsqlınstanceactivedirectoryadministrator</span><span class="sxs-lookup"><span data-stu-id="67ded-147">Get-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Get-AzSqlInstanceActiveDirectoryAdministrator.md)
