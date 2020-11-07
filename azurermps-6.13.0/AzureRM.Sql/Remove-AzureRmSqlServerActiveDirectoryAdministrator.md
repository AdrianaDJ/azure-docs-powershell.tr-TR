---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: B2E6E66A-1A09-4DB0-8BB4-D2E5EC34C9EB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqlserveractivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerActiveDirectoryAdministrator.md
ms.openlocfilehash: c8b186c55161732a014e281162fa5d6131e72115
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593625"
---
# <span data-ttu-id="a1cd4-101">Remove-AzureRmSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="a1cd4-101">Remove-AzureRmSqlServerActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="a1cd4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a1cd4-102">SYNOPSIS</span></span>
<span data-ttu-id="a1cd4-103">SQL Server için Azure AD yöneticisi 'ni kaldırır.</span><span class="sxs-lookup"><span data-stu-id="a1cd4-103">Removes an Azure AD administrator for SQL Server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a1cd4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a1cd4-104">SYNTAX</span></span>

```
Remove-AzureRmSqlServerActiveDirectoryAdministrator [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a1cd4-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a1cd4-105">DESCRIPTION</span></span>
<span data-ttu-id="a1cd4-106">**Remove-AzureRmSqlServerActiveDirectoryAdministrator** cmdlet 'i, geçerli abonelikteki AzureSQL Server Için Azure Active Directory (Azure AD) yöneticisini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="a1cd4-106">The **Remove-AzureRmSqlServerActiveDirectoryAdministrator** cmdlet removes an Azure Active Directory (Azure AD) administrator for AzureSQL Server in the current subscription.</span></span>

## <span data-ttu-id="a1cd4-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a1cd4-107">EXAMPLES</span></span>

### <span data-ttu-id="a1cd4-108">Örnek 1: yöneticiyi kaldırma</span><span class="sxs-lookup"><span data-stu-id="a1cd4-108">Example 1: Remove an administrator</span></span>
```
PS C:\>Remove-AzureRmSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
Confirm 
Are you sure you want to remove the Azure Sql Server Active Directory Administrator on server 'Server01'? 
[Y] Yes [A] Yes to All [N] No [L] No to All [S] Suspend [?] Help (default is "Y"): Y 

ResourceGroupName ServerName DisplayName ObjectId 
----------------- ---------- ----------- -------- 
ResourceGroup01   Server01   DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="a1cd4-109">Bu komut, kaynak grubuyla ilişkili server01 adlı sunucu için Azure AD yöneticisi 'ni kaldırır.</span><span class="sxs-lookup"><span data-stu-id="a1cd4-109">This command removes the Azure AD administrator for the server named Server01 associated with the resource group ResourceGroup01.</span></span>

## <span data-ttu-id="a1cd4-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a1cd4-110">PARAMETERS</span></span>

### <span data-ttu-id="a1cd4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1cd4-111">-DefaultProfile</span></span>
<span data-ttu-id="a1cd4-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="a1cd4-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a1cd4-113">-Force</span><span class="sxs-lookup"><span data-stu-id="a1cd4-113">-Force</span></span>
<span data-ttu-id="a1cd4-114">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="a1cd4-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a1cd4-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1cd4-115">-ResourceGroupName</span></span>
<span data-ttu-id="a1cd4-116">SQL Server 'ın atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a1cd4-116">Specifies the name of the resource group to which the SQL Server is assigned.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1cd4-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="a1cd4-117">-ServerName</span></span>
<span data-ttu-id="a1cd4-118">Bu cmdlet 'in bir yöneticiyi kaldırdığı SQL Server 'ın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a1cd4-118">Specifies the name of the SQL Server for which this cmdlet removes an administrator.</span></span>

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

### <span data-ttu-id="a1cd4-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="a1cd4-119">-Confirm</span></span>
<span data-ttu-id="a1cd4-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a1cd4-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1cd4-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1cd4-121">-WhatIf</span></span>
<span data-ttu-id="a1cd4-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a1cd4-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a1cd4-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a1cd4-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1cd4-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1cd4-124">CommonParameters</span></span>
<span data-ttu-id="a1cd4-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a1cd4-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1cd4-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1cd4-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1cd4-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a1cd4-127">INPUTS</span></span>

### <span data-ttu-id="a1cd4-128">System. String</span><span class="sxs-lookup"><span data-stu-id="a1cd4-128">System.String</span></span>

## <span data-ttu-id="a1cd4-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a1cd4-129">OUTPUTS</span></span>

### <span data-ttu-id="a1cd4-130">Microsoft. Azure. Commands. Sql. ServerActiveDirectoryAdministrator. model. Azureskreserveractivedirectoryadministratormodel</span><span class="sxs-lookup"><span data-stu-id="a1cd4-130">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryAdministratorModel</span></span>

## <span data-ttu-id="a1cd4-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a1cd4-131">NOTES</span></span>

## <span data-ttu-id="a1cd4-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a1cd4-132">RELATED LINKS</span></span>

[<span data-ttu-id="a1cd4-133">Get-AzureRmSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="a1cd4-133">Get-AzureRmSqlServerActiveDirectoryAdministrator</span></span>](./Get-AzureRmSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="a1cd4-134">Set-AzureRmSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="a1cd4-134">Set-AzureRmSqlServerActiveDirectoryAdministrator</span></span>](./Set-AzureRmSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="a1cd4-135">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="a1cd4-135">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

