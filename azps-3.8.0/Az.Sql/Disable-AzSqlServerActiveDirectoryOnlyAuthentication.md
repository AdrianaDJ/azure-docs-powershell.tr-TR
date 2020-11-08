---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/disable-azsqlserveractivedirectoryonlyauthentication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlServerActiveDirectoryOnlyAuthentication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlServerActiveDirectoryOnlyAuthentication.md
ms.openlocfilehash: a736ede2c84b3fbe782928d7cff14a558b69bcdf
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097495"
---
# <span data-ttu-id="f1ff9-101">Disable-AzSqlServerActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="f1ff9-101">Disable-AzSqlServerActiveDirectoryOnlyAuthentication</span></span>

## <span data-ttu-id="f1ff9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f1ff9-102">SYNOPSIS</span></span>
<span data-ttu-id="f1ff9-103">Belirli bir SQL Server için Azure AD only kimlik doğrulamasını devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="f1ff9-103">Disables Azure AD only authentication for a specific SQL Server.</span></span>

## <span data-ttu-id="f1ff9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f1ff9-104">SYNTAX</span></span>

```
Disable-AzSqlServerActiveDirectoryOnlyAuthentication [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f1ff9-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f1ff9-105">DESCRIPTION</span></span>
<span data-ttu-id="f1ff9-106">**Disable-AzSqlServerActiveDirectoryOnlyAuthentication** cmdlet 'i geçerli abonelikteki bir AzureSQL Server Için Azure Active Directory (Azure AD) kimlik doğrulama gereksinimini devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="f1ff9-106">The **Disable-AzSqlServerActiveDirectoryOnlyAuthentication** cmdlet disables Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL Server in the current subscription.</span></span>

## <span data-ttu-id="f1ff9-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f1ff9-107">EXAMPLES</span></span>

### <span data-ttu-id="f1ff9-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="f1ff9-108">Example 1</span></span>
```powershell
PS C:\>Disable-AzSqlServerActiveDirectoryOnlyAuthentication -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ResourceGroupName ServerName DisplayName ObjectId IsAzureADOnlyAuthentication
----------------- ---------- ----------- -------- -----------
ResourceGroup01   Server01   DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b False
```

<span data-ttu-id="f1ff9-109">Bu komut, ResourceGroup01 adlı bir kaynak grubuyla ilişkilendirilmiş server01 adlı bir AzureSQL sunucusu için Azure Active Directory (Azure AD) kimlik doğrulama gereksinimini devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="f1ff9-109">This command disables Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL server named Server01 that is associated with a resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="f1ff9-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f1ff9-110">PARAMETERS</span></span>

### <span data-ttu-id="f1ff9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1ff9-111">-DefaultProfile</span></span>
<span data-ttu-id="f1ff9-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f1ff9-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1ff9-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1ff9-113">-ResourceGroupName</span></span>
<span data-ttu-id="f1ff9-114">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="f1ff9-114">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1ff9-115">-ServerName</span><span class="sxs-lookup"><span data-stu-id="f1ff9-115">-ServerName</span></span>
<span data-ttu-id="f1ff9-116">Azure Active Directory Yöneticisi 'nde Azure SQL Server 'ın adı.</span><span class="sxs-lookup"><span data-stu-id="f1ff9-116">The name of the Azure SQL Server the Azure Active Directory administrator is in.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1ff9-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="f1ff9-117">-Confirm</span></span>
<span data-ttu-id="f1ff9-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f1ff9-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1ff9-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1ff9-119">-WhatIf</span></span>
<span data-ttu-id="f1ff9-120">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f1ff9-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f1ff9-121">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f1ff9-121">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1ff9-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1ff9-122">CommonParameters</span></span>
<span data-ttu-id="f1ff9-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f1ff9-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1ff9-124">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="f1ff9-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1ff9-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f1ff9-125">INPUTS</span></span>

### <span data-ttu-id="f1ff9-126">System. String</span><span class="sxs-lookup"><span data-stu-id="f1ff9-126">System.String</span></span>

## <span data-ttu-id="f1ff9-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f1ff9-127">OUTPUTS</span></span>

### <span data-ttu-id="f1ff9-128">Microsoft. Azure. Commands. Sql. ServerActiveDirectoryAdministrator. model. Azureskreserveractivedirectoryadministratormodel</span><span class="sxs-lookup"><span data-stu-id="f1ff9-128">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryAdministratorModel</span></span>

## <span data-ttu-id="f1ff9-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f1ff9-129">NOTES</span></span>

## <span data-ttu-id="f1ff9-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f1ff9-130">RELATED LINKS</span></span>

[<span data-ttu-id="f1ff9-131">Remove-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="f1ff9-131">Remove-AzSqlServerActiveDirectoryAdministrator</span></span>](./Remove-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="f1ff9-132">Set-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="f1ff9-132">Set-AzSqlServerActiveDirectoryAdministrator</span></span>](./Set-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="f1ff9-133">Get-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="f1ff9-133">Get-AzSqlServerActiveDirectoryAdministrator</span></span>](./Get-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="f1ff9-134">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="f1ff9-134">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)