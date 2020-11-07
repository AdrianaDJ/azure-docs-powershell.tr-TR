---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: D3BA6534-CAAC-41E2-8442-0606B712E2B8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseAuditing.md
ms.openlocfilehash: 30161db97a108b4a5612eb9fbf0d3d749b64a11e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93765053"
---
# <span data-ttu-id="8e629-101">Remove-AzureRmSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="8e629-101">Remove-AzureRmSqlDatabaseAuditing</span></span>

## <span data-ttu-id="8e629-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8e629-102">SYNOPSIS</span></span>
<span data-ttu-id="8e629-103">Veritabanının denetimini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="8e629-103">Removes the auditing of a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8e629-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8e629-104">SYNTAX</span></span>

```
Remove-AzureRmSqlDatabaseAuditing [-PassThru] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8e629-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="8e629-105">DESCRIPTION</span></span>
<span data-ttu-id="8e629-106">**Remove-AzureRmSqlDatabaseAuditing** cmdlet 'i, BIR Azure SQL veritabanının denetimini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="8e629-106">The **Remove-AzureRmSqlDatabaseAuditing** cmdlet removes the auditing of an Azure SQL database.</span></span>
<span data-ttu-id="8e629-107">Bu cmdlet 'i kullanmak için, *Resourcegroupname* , *ServerName* ve *DatabaseName* parametrelerini kullanarak veritabanını belirleyin.</span><span class="sxs-lookup"><span data-stu-id="8e629-107">To use this cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="8e629-108">Bu cmdlet 'i çalıştırdıktan sonra, veritabanı denetimi yapılmaz.</span><span class="sxs-lookup"><span data-stu-id="8e629-108">After you run this cmdlet, auditing of the database is not performed.</span></span>
<span data-ttu-id="8e629-109">Komut başarılı olur ve *geçiş parametresini kullandıysanız* , cmdlet, veritabanı tanımlayıcılarının yanı sıra geçerli denetim ilkesini tanımlayan bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="8e629-109">If the command succeeds and you have used the *PassThru* parameter, the cmdlet returns an object that describes the current auditing policy, in addition to the database identifiers.</span></span>
<span data-ttu-id="8e629-110">Veritabanı tanımlayıcıları, **Resourcegroupname** , **ServerName** ve **DatabaseName** ile sınırlı değildir.</span><span class="sxs-lookup"><span data-stu-id="8e629-110">Database identifiers include, but are not limited to, the **ResourceGroupName** , **ServerName** and **DatabaseName**.</span></span>

<span data-ttu-id="8e629-111">Bir Azure SQL veritabanının denetimini kaldırırsanız, tehdit algılama de kaldırılır.</span><span class="sxs-lookup"><span data-stu-id="8e629-111">If you remove auditing of an Azure SQL database, threat detection is also removed.</span></span>

<span data-ttu-id="8e629-112">Bu cmdlet, Azure 'da SQL Server genişletme veritabanı hizmeti tarafından da desteklenir.</span><span class="sxs-lookup"><span data-stu-id="8e629-112">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="8e629-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8e629-113">EXAMPLES</span></span>

### <span data-ttu-id="8e629-114">Örnek 1: Azure SQL veritabanı denetimini kaldırma</span><span class="sxs-lookup"><span data-stu-id="8e629-114">Example 1: Remove the auditing of an Azure SQL database</span></span>
```
PS C:\>Remove-AzureRmSqlDatabaseAuditing -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="8e629-115">Bu komut, Database01 adlı veritabanı denetimini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="8e629-115">This command removes the auditing of database named Database01.</span></span>
<span data-ttu-id="8e629-116">Bu veritabanı, ResourceGroup01 adındaki kaynak grubuna atanmış olan Server01 üzerinde bulunur.</span><span class="sxs-lookup"><span data-stu-id="8e629-116">That database is located on Server01, which is assigned to the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="8e629-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8e629-117">PARAMETERS</span></span>

### <span data-ttu-id="8e629-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="8e629-118">-DatabaseName</span></span>
<span data-ttu-id="8e629-119">Veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8e629-119">Specifies the name of the database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e629-120">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="8e629-120">-PassThru</span></span>
<span data-ttu-id="8e629-121">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="8e629-121">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="8e629-122">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="8e629-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="8e629-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e629-123">-ResourceGroupName</span></span>
<span data-ttu-id="8e629-124">Veritabanını içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8e629-124">Specifies the name of the resource group containing the database.</span></span>

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

### <span data-ttu-id="8e629-125">-ServerName</span><span class="sxs-lookup"><span data-stu-id="8e629-125">-ServerName</span></span>
<span data-ttu-id="8e629-126">Veritabanını içeren sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8e629-126">Specifies the name of the server containing the database.</span></span>

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

### <span data-ttu-id="8e629-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="8e629-127">-Confirm</span></span>
<span data-ttu-id="8e629-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="8e629-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e629-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e629-129">-WhatIf</span></span>
<span data-ttu-id="8e629-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="8e629-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8e629-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="8e629-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8e629-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e629-132">-DefaultProfile</span></span>
<span data-ttu-id="8e629-133">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8e629-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8e629-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e629-134">CommonParameters</span></span>
<span data-ttu-id="8e629-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8e629-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e629-136">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8e629-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e629-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8e629-137">INPUTS</span></span>

### <span data-ttu-id="8e629-138">Microsoft. Azure. Commands. Sql. Security. model. DatabaseAuditingPolicyModel</span><span class="sxs-lookup"><span data-stu-id="8e629-138">Microsoft.Azure.Commands.Sql.Security.Model.DatabaseAuditingPolicyModel</span></span>

## <span data-ttu-id="8e629-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8e629-139">OUTPUTS</span></span>

### <span data-ttu-id="8e629-140">Microsoft. Azure. Commands. Sql. Security. model. DatabaseAuditingPolicyModel</span><span class="sxs-lookup"><span data-stu-id="8e629-140">Microsoft.Azure.Commands.Sql.Security.Model.DatabaseAuditingPolicyModel</span></span>

## <span data-ttu-id="8e629-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8e629-141">NOTES</span></span>

## <span data-ttu-id="8e629-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8e629-142">RELATED LINKS</span></span>

[<span data-ttu-id="8e629-143">Get-AzureRmSqlDatabaseAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="8e629-143">Get-AzureRmSqlDatabaseAuditingPolicy</span></span>](./Get-AzureRmSqlDatabaseAuditingPolicy.md)

[<span data-ttu-id="8e629-144">Set-AzureRmSqlDatabaseAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="8e629-144">Set-AzureRmSqlDatabaseAuditingPolicy</span></span>](./Set-AzureRmSqlDatabaseAuditingPolicy.md)

[<span data-ttu-id="8e629-145">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="8e629-145">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


