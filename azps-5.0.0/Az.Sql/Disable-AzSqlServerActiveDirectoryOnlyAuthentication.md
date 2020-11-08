---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/disable-azsqlserveractivedirectoryonlyauthentication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlServerActiveDirectoryOnlyAuthentication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlServerActiveDirectoryOnlyAuthentication.md
ms.openlocfilehash: 8d9214b44d5e408717968d042a1cdb86cd25130a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94275677"
---
# <span data-ttu-id="ced26-101">Disable-AzSqlServerActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="ced26-101">Disable-AzSqlServerActiveDirectoryOnlyAuthentication</span></span>

## <span data-ttu-id="ced26-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ced26-102">SYNOPSIS</span></span>
<span data-ttu-id="ced26-103">Belirli bir SQL Server için Azure AD only kimlik doğrulamasını devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="ced26-103">Disables Azure AD only authentication for a specific SQL Server.</span></span>

## <span data-ttu-id="ced26-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ced26-104">SYNTAX</span></span>

### <span data-ttu-id="ced26-105">UseResourceGroupAndServerNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="ced26-105">UseResourceGroupAndServerNameParameterSet (Default)</span></span>
```
Disable-AzSqlServerActiveDirectoryOnlyAuthentication [-ResourceGroupName] <String> [-ServerName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ced26-106">UseInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ced26-106">UseInputObjectParameterSet</span></span>
```
Disable-AzSqlServerActiveDirectoryOnlyAuthentication -InputObject <AzureSqlServerModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ced26-107">Userresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="ced26-107">UserResourceIdParameterSet</span></span>
```
Disable-AzSqlServerActiveDirectoryOnlyAuthentication [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ced26-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="ced26-108">DESCRIPTION</span></span>
<span data-ttu-id="ced26-109">**Disable-AzSqlServerActiveDirectoryOnlyAuthentication** cmdlet 'i geçerli abonelikteki bir AzureSQL Server Için Azure Active Directory (Azure AD) kimlik doğrulama gereksinimini devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="ced26-109">The **Disable-AzSqlServerActiveDirectoryOnlyAuthentication** cmdlet disables Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL Server in the current subscription.</span></span>

## <span data-ttu-id="ced26-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ced26-110">EXAMPLES</span></span>

### <span data-ttu-id="ced26-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="ced26-111">Example 1</span></span>
```powershell
PS C:\>Disable-AzSqlServerActiveDirectoryOnlyAuthentication -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ResourceGroupName ServerName AzureADOnlyAuthentication
----------------- ---------- ----------- -------- -----------
ResourceGroup01   Server01   False
```

<span data-ttu-id="ced26-112">Bu komut, ResourceGroup01 adlı bir kaynak grubuyla ilişkilendirilmiş server01 adlı bir AzureSQL sunucusu için Azure Active Directory (Azure AD) kimlik doğrulama gereksinimini devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="ced26-112">This command disables Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL server named Server01 that is associated with a resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="ced26-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ced26-113">PARAMETERS</span></span>

### <span data-ttu-id="ced26-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ced26-114">-DefaultProfile</span></span>
<span data-ttu-id="ced26-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ced26-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ced26-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ced26-116">-InputObject</span></span>
<span data-ttu-id="ced26-117">Kullanılacak SQL Server nesnesi.</span><span class="sxs-lookup"><span data-stu-id="ced26-117">The SQL server object to use.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel
Parameter Sets: UseInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ced26-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ced26-118">-ResourceGroupName</span></span>
<span data-ttu-id="ced26-119">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="ced26-119">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: UseResourceGroupAndServerNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ced26-120">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="ced26-120">-ResourceId</span></span>
<span data-ttu-id="ced26-121">Kullanılacak örneğinin kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="ced26-121">The resource id of instance to use</span></span>

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

### <span data-ttu-id="ced26-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="ced26-122">-ServerName</span></span>
<span data-ttu-id="ced26-123">Azure SQL Server 'ın adı Azure Active Directory 'de yalnızca kimlik doğrulaması.</span><span class="sxs-lookup"><span data-stu-id="ced26-123">The name of the Azure SQL Server the Azure Active Directory only authentication is in.</span></span>

```yaml
Type: System.String
Parameter Sets: UseResourceGroupAndServerNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ced26-124">-Onay</span><span class="sxs-lookup"><span data-stu-id="ced26-124">-Confirm</span></span>
<span data-ttu-id="ced26-125">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ced26-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ced26-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ced26-126">-WhatIf</span></span>
<span data-ttu-id="ced26-127">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ced26-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ced26-128">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ced26-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ced26-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ced26-129">CommonParameters</span></span>
<span data-ttu-id="ced26-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ced26-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ced26-131">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="ced26-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ced26-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ced26-132">INPUTS</span></span>

### <span data-ttu-id="ced26-133">System. String</span><span class="sxs-lookup"><span data-stu-id="ced26-133">System.String</span></span>

## <span data-ttu-id="ced26-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ced26-134">OUTPUTS</span></span>

### <span data-ttu-id="ced26-135">Microsoft. Azure. Commands. Sql. ServerActiveDirectoryAdministrator. model. Azurescreserveractivedirectoryonlyauthenticationmodel</span><span class="sxs-lookup"><span data-stu-id="ced26-135">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryOnlyAuthenticationModel</span></span>

## <span data-ttu-id="ced26-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ced26-136">NOTES</span></span>

## <span data-ttu-id="ced26-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ced26-137">RELATED LINKS</span></span>

[<span data-ttu-id="ced26-138">Enable-AzSqlServerActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="ced26-138">Enable-AzSqlServerActiveDirectoryOnlyAuthentication</span></span>](./Enable-AzSqlServerActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="ced26-139">Get-AzSqlServerActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="ced26-139">Get-AzSqlServerActiveDirectoryOnlyAuthentication</span></span>](./Get-AzSqlServerActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="ced26-140">Set-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="ced26-140">Set-AzSqlServerActiveDirectoryAdministrator</span></span>](./Set-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="ced26-141">Get-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="ced26-141">Get-AzSqlServerActiveDirectoryAdministrator</span></span>](./Get-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="ced26-142">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="ced26-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)