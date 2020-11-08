---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserveractivedirectoryonlyauthentication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerActiveDirectoryOnlyAuthentication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerActiveDirectoryOnlyAuthentication.md
ms.openlocfilehash: e5460fcbc48d36dab6309891247315f0539ff7ab
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94107559"
---
# <span data-ttu-id="aa8cd-101">Get-AzSqlServerActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="aa8cd-101">Get-AzSqlServerActiveDirectoryOnlyAuthentication</span></span>

## <span data-ttu-id="aa8cd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aa8cd-102">SYNOPSIS</span></span>
<span data-ttu-id="aa8cd-103">Belirli bir SQL Server için Azure AD only kimlik doğrulamasını alır.</span><span class="sxs-lookup"><span data-stu-id="aa8cd-103">Gets Azure AD only authentication for a specific SQL Server.</span></span>

## <span data-ttu-id="aa8cd-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="aa8cd-104">SYNTAX</span></span>

### <span data-ttu-id="aa8cd-105">UseResourceGroupAndServerNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="aa8cd-105">UseResourceGroupAndServerNameParameterSet (Default)</span></span>
```
Get-AzSqlServerActiveDirectoryOnlyAuthentication [-ResourceGroupName] <String> [-ServerName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aa8cd-106">UseInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="aa8cd-106">UseInputObjectParameterSet</span></span>
```
Get-AzSqlServerActiveDirectoryOnlyAuthentication -InputObject <AzureSqlServerModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aa8cd-107">Userresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="aa8cd-107">UserResourceIdParameterSet</span></span>
```
Get-AzSqlServerActiveDirectoryOnlyAuthentication [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aa8cd-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="aa8cd-108">DESCRIPTION</span></span>
<span data-ttu-id="aa8cd-109">**Get-AzSqlServerActiveDirectoryOnlyAuthentication** cmdlet 'i, geçerli abonelikteki bir AzureSQL Server Için Azure Active Directory (Azure AD) kimlik doğrulama gereksinimini alır.</span><span class="sxs-lookup"><span data-stu-id="aa8cd-109">The **Get-AzSqlServerActiveDirectoryOnlyAuthentication** cmdlet gets Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL Server in the current subscription.</span></span>

## <span data-ttu-id="aa8cd-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="aa8cd-110">EXAMPLES</span></span>

### <span data-ttu-id="aa8cd-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="aa8cd-111">Example 1</span></span>
```powershell
PS C:\>Get-AzSqlServerActiveDirectoryOnlyAuthentication -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ResourceGroupName ServerName AzureADOnlyAuthentication
----------------- ---------- ----------- -------- -----------
ResourceGroup01   Server01   True
```

<span data-ttu-id="aa8cd-112">Bu komut, ResourceGroup01 adlı bir kaynak grubuyla ilişkilendirilmiş server01 adlı bir AzureSQL sunucusu için Azure Active Directory (Azure AD) kimlik doğrulama gereksinimini alır.</span><span class="sxs-lookup"><span data-stu-id="aa8cd-112">This command gets Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL server named Server01 that is associated with a resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="aa8cd-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="aa8cd-113">PARAMETERS</span></span>

### <span data-ttu-id="aa8cd-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa8cd-114">-DefaultProfile</span></span>
<span data-ttu-id="aa8cd-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="aa8cd-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aa8cd-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="aa8cd-116">-InputObject</span></span>
<span data-ttu-id="aa8cd-117">Kullanılacak SQL Server nesnesi.</span><span class="sxs-lookup"><span data-stu-id="aa8cd-117">The SQL server object to use.</span></span>

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

### <span data-ttu-id="aa8cd-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa8cd-118">-ResourceGroupName</span></span>
<span data-ttu-id="aa8cd-119">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="aa8cd-119">The name of the resource group.</span></span>

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

### <span data-ttu-id="aa8cd-120">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="aa8cd-120">-ResourceId</span></span>
<span data-ttu-id="aa8cd-121">Kullanılacak örneğinin kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="aa8cd-121">The resource id of instance to use</span></span>

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

### <span data-ttu-id="aa8cd-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="aa8cd-122">-ServerName</span></span>
<span data-ttu-id="aa8cd-123">Azure SQL Server 'ın adı Azure Active Directory 'de yalnızca kimlik doğrulaması.</span><span class="sxs-lookup"><span data-stu-id="aa8cd-123">The name of the Azure SQL Server the Azure Active Directory only authentication is in.</span></span>

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

### <span data-ttu-id="aa8cd-124">-Onay</span><span class="sxs-lookup"><span data-stu-id="aa8cd-124">-Confirm</span></span>
<span data-ttu-id="aa8cd-125">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="aa8cd-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aa8cd-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa8cd-126">-WhatIf</span></span>
<span data-ttu-id="aa8cd-127">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="aa8cd-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aa8cd-128">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="aa8cd-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aa8cd-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa8cd-129">CommonParameters</span></span>
<span data-ttu-id="aa8cd-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="aa8cd-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa8cd-131">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="aa8cd-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa8cd-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="aa8cd-132">INPUTS</span></span>

### <span data-ttu-id="aa8cd-133">System. String</span><span class="sxs-lookup"><span data-stu-id="aa8cd-133">System.String</span></span>

## <span data-ttu-id="aa8cd-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="aa8cd-134">OUTPUTS</span></span>

### <span data-ttu-id="aa8cd-135">Microsoft. Azure. Commands. Sql. ServerActiveDirectoryAdministrator. model. Azurescreserveractivedirectoryonlyauthenticationmodel</span><span class="sxs-lookup"><span data-stu-id="aa8cd-135">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryOnlyAuthenticationModel</span></span>

## <span data-ttu-id="aa8cd-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="aa8cd-136">NOTES</span></span>

## <span data-ttu-id="aa8cd-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="aa8cd-137">RELATED LINKS</span></span>

[<span data-ttu-id="aa8cd-138">Enable-AzSqlServerActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="aa8cd-138">Enable-AzSqlServerActiveDirectoryOnlyAuthentication</span></span>](./Enable-AzSqlServerActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="aa8cd-139">Disable-AzSqlServerActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="aa8cd-139">Disable-AzSqlServerActiveDirectoryOnlyAuthentication</span></span>](./Disable-AzSqlServerActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="aa8cd-140">Set-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="aa8cd-140">Set-AzSqlServerActiveDirectoryAdministrator</span></span>](./Set-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="aa8cd-141">Get-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="aa8cd-141">Get-AzSqlServerActiveDirectoryAdministrator</span></span>](./Get-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="aa8cd-142">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="aa8cd-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)