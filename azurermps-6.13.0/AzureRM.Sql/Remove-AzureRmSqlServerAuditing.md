---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 692D0B64-95EB-4D36-975F-65674B3B2F8C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqlserverauditing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerAuditing.md
ms.openlocfilehash: 3e43a61c95120b0f07f89e3f3fb64aab2dee8dff
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590825"
---
# <span data-ttu-id="5cd89-101">Remove-AzureRmSqlServerAuditing</span><span class="sxs-lookup"><span data-stu-id="5cd89-101">Remove-AzureRmSqlServerAuditing</span></span>

## <span data-ttu-id="5cd89-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5cd89-102">SYNOPSIS</span></span>
<span data-ttu-id="5cd89-103">SQL Server denetimini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="5cd89-103">Removes the auditing of a SQL server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5cd89-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5cd89-104">SYNTAX</span></span>

```
Remove-AzureRmSqlServerAuditing [-PassThru] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5cd89-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="5cd89-105">DESCRIPTION</span></span>
<span data-ttu-id="5cd89-106">**Remove-AzureRmSqlServerAuditing** cmdlet 'ı, Azure SQL Server 'ın denetimini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="5cd89-106">The **Remove-AzureRmSqlServerAuditing** cmdlet removes the auditing of an Azure SQL server.</span></span>
<span data-ttu-id="5cd89-107">Bu cmdlet 'i kullanmak için, sunucuyu tanımlayan *Resourcegroupname* ve *ServerName* parametrelerini belirtin.</span><span class="sxs-lookup"><span data-stu-id="5cd89-107">To use this cmdlet, specify the *ResourceGroupName* and *ServerName* parameters to identify the server.</span></span>
<span data-ttu-id="5cd89-108">Bu cmdlet 'i çalıştırdıktan sonra, Azure SQL Server 'daki veritabanlarının denetimi yapılmaz.</span><span class="sxs-lookup"><span data-stu-id="5cd89-108">After you run this cmdlet, auditing of the databases on the Azure SQL server is not performed.</span></span>
<span data-ttu-id="5cd89-109">Komut başarılı olur ve *geçiş parametresini belirtirseniz* cmdlet, geçerli denetim Ilkesini ve Azure SQL Server tanımlayıcılarını tanımlayan bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="5cd89-109">If the command succeeds, and you specify the *PassThru* parameter, the cmdlet returns an object that describes the current auditing policy and the Azure SQL server identifiers.</span></span>
<span data-ttu-id="5cd89-110">Sunucu tanımlayıcıları, **Resourcegroupname** ve **ServerName** 'i içerir.</span><span class="sxs-lookup"><span data-stu-id="5cd89-110">Server identifiers include the **ResourceGroupName** and **ServerName**.</span></span>

## <span data-ttu-id="5cd89-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5cd89-111">EXAMPLES</span></span>

### <span data-ttu-id="5cd89-112">Örnek 1: Azure SQL Server 'ın denetimini kaldırma</span><span class="sxs-lookup"><span data-stu-id="5cd89-112">Example 1: Remove the auditing of an Azure SQL server</span></span>
```
PS C:\>Remove-AzureRmSqlServerAuditing -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="5cd89-113">Bu komut, kaynak grubundaki server01 'de bulunan tüm veritabanlarının denetimini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="5cd89-113">This command removes the auditing of all the databases located on Server01 in resource group.</span></span>

## <span data-ttu-id="5cd89-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5cd89-114">PARAMETERS</span></span>

### <span data-ttu-id="5cd89-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5cd89-115">-DefaultProfile</span></span>
<span data-ttu-id="5cd89-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="5cd89-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5cd89-117">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="5cd89-117">-PassThru</span></span>
<span data-ttu-id="5cd89-118">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="5cd89-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="5cd89-119">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="5cd89-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="5cd89-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5cd89-120">-ResourceGroupName</span></span>
<span data-ttu-id="5cd89-121">Azure SQL Server 'ın atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5cd89-121">Specifies the name of the resource group to which the Azure SQL server is assigned.</span></span>

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

### <span data-ttu-id="5cd89-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="5cd89-122">-ServerName</span></span>
<span data-ttu-id="5cd89-123">Azure SQL Server 'ın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5cd89-123">Specifies the name of the Azure SQL server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5cd89-124">-Onay</span><span class="sxs-lookup"><span data-stu-id="5cd89-124">-Confirm</span></span>
<span data-ttu-id="5cd89-125">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="5cd89-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5cd89-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5cd89-126">-WhatIf</span></span>
<span data-ttu-id="5cd89-127">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5cd89-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5cd89-128">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="5cd89-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5cd89-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5cd89-129">CommonParameters</span></span>
<span data-ttu-id="5cd89-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5cd89-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5cd89-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5cd89-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5cd89-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5cd89-132">INPUTS</span></span>

### <span data-ttu-id="5cd89-133">System. String</span><span class="sxs-lookup"><span data-stu-id="5cd89-133">System.String</span></span>

## <span data-ttu-id="5cd89-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5cd89-134">OUTPUTS</span></span>

### <span data-ttu-id="5cd89-135">Microsoft. Azure. Commands. Sql. Auditing. model. AuditingPolicyModel</span><span class="sxs-lookup"><span data-stu-id="5cd89-135">Microsoft.Azure.Commands.Sql.Auditing.Model.AuditingPolicyModel</span></span>

## <span data-ttu-id="5cd89-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5cd89-136">NOTES</span></span>

## <span data-ttu-id="5cd89-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5cd89-137">RELATED LINKS</span></span>

[<span data-ttu-id="5cd89-138">Get-AzureRmSqlDatabaseAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="5cd89-138">Get-AzureRmSqlDatabaseAuditingPolicy</span></span>](./Get-AzureRmSqlDatabaseAuditingPolicy.md)

[<span data-ttu-id="5cd89-139">Set-AzureRmSqlDatabaseAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="5cd89-139">Set-AzureRmSqlDatabaseAuditingPolicy</span></span>](./Set-AzureRmSqlDatabaseAuditingPolicy.md)

[<span data-ttu-id="5cd89-140">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="5cd89-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


