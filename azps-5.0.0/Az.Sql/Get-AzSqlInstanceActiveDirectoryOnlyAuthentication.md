---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstanceactivedirectoryonlyauthentication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceActiveDirectoryOnlyAuthentication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceActiveDirectoryOnlyAuthentication.md
ms.openlocfilehash: 10788eea0c3571450a483888945ab591d7ddf13b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94322077"
---
# <span data-ttu-id="d0ac2-101">Get-AzSqlInstanceActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="d0ac2-101">Get-AzSqlInstanceActiveDirectoryOnlyAuthentication</span></span>

## <span data-ttu-id="d0ac2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d0ac2-102">SYNOPSIS</span></span>
<span data-ttu-id="d0ac2-103">Belirli bir SQL yönetilen örneği için Azure AD only kimlik doğrulamasını alır.</span><span class="sxs-lookup"><span data-stu-id="d0ac2-103">Gets Azure AD only authentication for a specific SQL Managed Instance.</span></span>

## <span data-ttu-id="d0ac2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d0ac2-104">SYNTAX</span></span>

### <span data-ttu-id="d0ac2-105">Useresourcegroupandınstancenameparameterset (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d0ac2-105">UseResourceGroupAndInstanceNameParameterSet (Default)</span></span>
```
Get-AzSqlInstanceActiveDirectoryOnlyAuthentication [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d0ac2-106">UseInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d0ac2-106">UseInputObjectParameterSet</span></span>
```
Get-AzSqlInstanceActiveDirectoryOnlyAuthentication -InputObject <AzureSqlManagedInstanceModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d0ac2-107">Userresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="d0ac2-107">UserResourceIdParameterSet</span></span>
```
Get-AzSqlInstanceActiveDirectoryOnlyAuthentication [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d0ac2-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="d0ac2-108">DESCRIPTION</span></span>
<span data-ttu-id="d0ac2-109">**Get-Azsqlınstanceactivedirectoryonlyauthentication** cmdlet 'i, geçerli abonelikteki bir AzureSQL yönetilen örneği Için Azure Active Directory (Azure AD) kimlik doğrulama gereksinimini alır.</span><span class="sxs-lookup"><span data-stu-id="d0ac2-109">The **Get-AzSqlInstanceActiveDirectoryOnlyAuthentication** cmdlet gets Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL Managed Instance in the current subscription.</span></span>

## <span data-ttu-id="d0ac2-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d0ac2-110">EXAMPLES</span></span>

### <span data-ttu-id="d0ac2-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="d0ac2-111">Example 1</span></span>
```powershell
PS C:\>Get-AzSqlInstanceActiveDirectoryOnlyAuthentication -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01"
```

<span data-ttu-id="d0ac2-112">Bu komut, ResourceGroup01 adlı bir kaynak grubuyla ilişkilendirilmiş ManagedInstance01 adlı bir AzureSQL yönetilen örneğinin Azure Active Directory (Azure AD) kimlik doğrulama gereksinimini alır.</span><span class="sxs-lookup"><span data-stu-id="d0ac2-112">This command gets Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL Managed Instance named ManagedInstance01 that is associated with a resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="d0ac2-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d0ac2-113">PARAMETERS</span></span>

### <span data-ttu-id="d0ac2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0ac2-114">-DefaultProfile</span></span>
<span data-ttu-id="d0ac2-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d0ac2-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d0ac2-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d0ac2-116">-InputObject</span></span>
<span data-ttu-id="d0ac2-117">Kullanılacak yönetilen örnek nesnesi.</span><span class="sxs-lookup"><span data-stu-id="d0ac2-117">The managed instance object to use.</span></span>

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

### <span data-ttu-id="d0ac2-118">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="d0ac2-118">-InstanceName</span></span>
<span data-ttu-id="d0ac2-119">Azure SQL yönetilen örneğinin adı Azure Active Directory 'de yalnızca kimlik doğrulaması içinde.</span><span class="sxs-lookup"><span data-stu-id="d0ac2-119">The name of the Azure SQL Managed Instance the Azure Active Directory only authentication is in.</span></span>

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

### <span data-ttu-id="d0ac2-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0ac2-120">-ResourceGroupName</span></span>
<span data-ttu-id="d0ac2-121">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="d0ac2-121">The name of the resource group.</span></span>

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

### <span data-ttu-id="d0ac2-122">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="d0ac2-122">-ResourceId</span></span>
<span data-ttu-id="d0ac2-123">Kullanılacak örneğinin kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="d0ac2-123">The resource id of instance to use</span></span>

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

### <span data-ttu-id="d0ac2-124">-Onay</span><span class="sxs-lookup"><span data-stu-id="d0ac2-124">-Confirm</span></span>
<span data-ttu-id="d0ac2-125">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d0ac2-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d0ac2-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0ac2-126">-WhatIf</span></span>
<span data-ttu-id="d0ac2-127">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d0ac2-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d0ac2-128">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d0ac2-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d0ac2-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0ac2-129">CommonParameters</span></span>
<span data-ttu-id="d0ac2-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d0ac2-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0ac2-131">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="d0ac2-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0ac2-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d0ac2-132">INPUTS</span></span>

### <span data-ttu-id="d0ac2-133">System. String</span><span class="sxs-lookup"><span data-stu-id="d0ac2-133">System.String</span></span>

## <span data-ttu-id="d0ac2-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d0ac2-134">OUTPUTS</span></span>

### <span data-ttu-id="d0ac2-135">Microsoft. Azure. Commands. Sql. ınstanceactivedirectoryonlyauthentication. model. azures, ınstanceactivedirectoryonlyauthenticationmodel</span><span class="sxs-lookup"><span data-stu-id="d0ac2-135">Microsoft.Azure.Commands.Sql.InstanceActiveDirectoryOnlyAuthentication.Model.AzureSqlInstanceActiveDirectoryOnlyAuthenticationModel</span></span>

## <span data-ttu-id="d0ac2-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d0ac2-136">NOTES</span></span>

## <span data-ttu-id="d0ac2-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d0ac2-137">RELATED LINKS</span></span>

[<span data-ttu-id="d0ac2-138">Enable-Azsqlınstanceactivedirectoryonlyauthentication</span><span class="sxs-lookup"><span data-stu-id="d0ac2-138">Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication</span></span>](./Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="d0ac2-139">Disable-Azsqlınstanceactivedirectoryonlyauthentication</span><span class="sxs-lookup"><span data-stu-id="d0ac2-139">Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication</span></span>](./Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="d0ac2-140">Set-Azsqlınstanceactivedirectoryadministrator</span><span class="sxs-lookup"><span data-stu-id="d0ac2-140">Set-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Set-AzSqlInstanceActiveDirectoryAdministrator.md)

[<span data-ttu-id="d0ac2-141">Get-Azsqlınstanceactivedirectoryadministrator</span><span class="sxs-lookup"><span data-stu-id="d0ac2-141">Get-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Get-AzSqlInstanceActiveDirectoryAdministrator.md)

