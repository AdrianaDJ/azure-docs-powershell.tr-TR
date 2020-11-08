---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/disable-azsqlinstanceactivedirectoryonlyauthentication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication.md
ms.openlocfilehash: 5f4ee759fcfddf8e68bc41b68706ccaf2d582e96
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94278167"
---
# <span data-ttu-id="3892a-101">Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="3892a-101">Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication</span></span>

## <span data-ttu-id="3892a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3892a-102">SYNOPSIS</span></span>
<span data-ttu-id="3892a-103">Belirli bir SQL yönetilen örneği için Azure AD only kimlik doğrulamasını devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="3892a-103">Disables Azure AD only authentication for a specific SQL Managed Instance.</span></span>

## <span data-ttu-id="3892a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3892a-104">SYNTAX</span></span>

### <span data-ttu-id="3892a-105">Useresourcegroupandınstancenameparameterset (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="3892a-105">UseResourceGroupAndInstanceNameParameterSet (Default)</span></span>
```
Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3892a-106">UseInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3892a-106">UseInputObjectParameterSet</span></span>
```
Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication -InputObject <AzureSqlManagedInstanceModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3892a-107">Userresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="3892a-107">UserResourceIdParameterSet</span></span>
```
Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3892a-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="3892a-108">DESCRIPTION</span></span>
<span data-ttu-id="3892a-109">**Disable-Azsqlınstanceactivedirectoryonlyauthentication** cmdlet 'i geçerli abonelikteki bir AzureSQL yönetilen örneği Için Azure Active Directory (Azure AD) kimlik doğrulama gereksinimini devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="3892a-109">The **Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication** cmdlet disables Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL Managed Instance in the current subscription.</span></span>

## <span data-ttu-id="3892a-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3892a-110">EXAMPLES</span></span>

### <span data-ttu-id="3892a-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="3892a-111">Example 1</span></span>
```powershell
PS C:\>Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01"
ResourceGroupName InstanceName        AzureADOnlyAuthentication
----------------- ---------- ----------- -------- -----------
ResourceGroup01   ManagedInstance01   True
```

<span data-ttu-id="3892a-112">Bu komut, ResourceGroup01 adlı bir kaynak grubuyla ilişkilendirilmiş ManagedInstance01 adlı bir AzureSQL yönetilen örneğinin Azure Active Directory (Azure AD) kimlik doğrulama gereksinimini devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="3892a-112">This command disables Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL Managed Instance named ManagedInstance01 that is associated with a resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="3892a-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3892a-113">PARAMETERS</span></span>

### <span data-ttu-id="3892a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3892a-114">-DefaultProfile</span></span>
<span data-ttu-id="3892a-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3892a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3892a-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3892a-116">-InputObject</span></span>
<span data-ttu-id="3892a-117">Kullanılacak yönetilen örnek nesnesi.</span><span class="sxs-lookup"><span data-stu-id="3892a-117">The managed instance object to use.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel
Parameter Sets: UseInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3892a-118">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="3892a-118">-InstanceName</span></span>
<span data-ttu-id="3892a-119">Azure SQL yönetilen örneğinin adı Azure Active Directory 'de yalnızca kimlik doğrulaması içinde.</span><span class="sxs-lookup"><span data-stu-id="3892a-119">The name of the Azure SQL Managed Instance the Azure Active Directory only authentication is in.</span></span>

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

### <span data-ttu-id="3892a-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3892a-120">-ResourceGroupName</span></span>
<span data-ttu-id="3892a-121">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="3892a-121">The name of the resource group.</span></span>

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

### <span data-ttu-id="3892a-122">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="3892a-122">-ResourceId</span></span>
<span data-ttu-id="3892a-123">Kullanılacak örneğinin kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="3892a-123">The resource id of instance to use</span></span>

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

### <span data-ttu-id="3892a-124">-Onay</span><span class="sxs-lookup"><span data-stu-id="3892a-124">-Confirm</span></span>
<span data-ttu-id="3892a-125">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="3892a-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3892a-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3892a-126">-WhatIf</span></span>
<span data-ttu-id="3892a-127">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3892a-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3892a-128">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="3892a-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3892a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3892a-129">CommonParameters</span></span>
<span data-ttu-id="3892a-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3892a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3892a-131">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="3892a-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3892a-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3892a-132">INPUTS</span></span>

### <span data-ttu-id="3892a-133">System. String</span><span class="sxs-lookup"><span data-stu-id="3892a-133">System.String</span></span>

## <span data-ttu-id="3892a-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3892a-134">OUTPUTS</span></span>

### <span data-ttu-id="3892a-135">Microsoft. Azure. Commands. Sql. ınstanceactivedirectoryonlyauthentication. model. azures, ınstanceactivedirectoryonlyauthenticationmodel</span><span class="sxs-lookup"><span data-stu-id="3892a-135">Microsoft.Azure.Commands.Sql.InstanceActiveDirectoryOnlyAuthentication.Model.AzureSqlInstanceActiveDirectoryOnlyAuthenticationModel</span></span>

## <span data-ttu-id="3892a-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3892a-136">NOTES</span></span>

## <span data-ttu-id="3892a-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3892a-137">RELATED LINKS</span></span>

[<span data-ttu-id="3892a-138">Enable-Azsqlınstanceactivedirectoryonlyauthentication</span><span class="sxs-lookup"><span data-stu-id="3892a-138">Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication</span></span>](./Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="3892a-139">Get-Azsqlınstanceactivedirectoryonlyauthentication</span><span class="sxs-lookup"><span data-stu-id="3892a-139">Get-AzSqlInstanceActiveDirectoryOnlyAuthentication</span></span>](./Get-AzSqlInstanceActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="3892a-140">Set-Azsqlınstanceactivedirectoryadministrator</span><span class="sxs-lookup"><span data-stu-id="3892a-140">Set-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Set-AzSqlInstanceActiveDirectoryAdministrator.md)

[<span data-ttu-id="3892a-141">Get-Azsqlınstanceactivedirectoryadministrator</span><span class="sxs-lookup"><span data-stu-id="3892a-141">Get-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Get-AzSqlInstanceActiveDirectoryAdministrator.md)