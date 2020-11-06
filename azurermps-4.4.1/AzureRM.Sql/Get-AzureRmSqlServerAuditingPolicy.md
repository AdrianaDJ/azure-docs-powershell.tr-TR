---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 40674DC7-E35F-4C9F-8CE0-D1C6F524C9FB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerAuditingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerAuditingPolicy.md
ms.openlocfilehash: 34eedd81d5e8625ed957cba16d3cec1ea33a0c32
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590607"
---
# <span data-ttu-id="b2c8d-101">Get-AzureRmSqlServerAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="b2c8d-101">Get-AzureRmSqlServerAuditingPolicy</span></span>

## <span data-ttu-id="b2c8d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b2c8d-102">SYNOPSIS</span></span>
<span data-ttu-id="b2c8d-103">SQL Server 'ın denetim ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="b2c8d-103">Gets the auditing policy of a SQL server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b2c8d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b2c8d-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerAuditingPolicy -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b2c8d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b2c8d-105">DESCRIPTION</span></span>
<span data-ttu-id="b2c8d-106">**Get-AzureRmSqlServerAuditingPolicy** cmdlet 'i, BIR Azure SQL Server 'ın denetim ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="b2c8d-106">The **Get-AzureRmSqlServerAuditingPolicy** cmdlet gets the auditing policy of an Azure SQL server.</span></span>
<span data-ttu-id="b2c8d-107">Veritabanını tanımlamak için *Resourcegroupname* , *ServerName* ve *DatabaseName* parametrelerini belirtin.</span><span class="sxs-lookup"><span data-stu-id="b2c8d-107">Specify the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="b2c8d-108">Bu cmdlet, belirtilen Azure SQL Server 'da tanımlı olan Azure SQL veritabanları tarafından kullanılan bir ilkeyi döndürür ve denetim ilkesini kullanır.</span><span class="sxs-lookup"><span data-stu-id="b2c8d-108">This cmdlet returns a policy that is used by the Azure SQL databases that are both defined in the specified Azure SQL server and use its auditing policy.</span></span>

## <span data-ttu-id="b2c8d-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b2c8d-109">EXAMPLES</span></span>

### <span data-ttu-id="b2c8d-110">Örnek 1: bir Azure SQL Server 'ın üzerinde tablo denetimi tanımlanmış denetim ilkesini alma</span><span class="sxs-lookup"><span data-stu-id="b2c8d-110">Example 1: Get the auditing policy of an Azure SQL server with Table auditing defined on it</span></span>
```
PS C:\>Get-AzureRmSqlServerAuditingPolicy -ResourceGroupName "resourcegroup01" -ServerName "server01"
EventType              : {PlainSQL_Success, PlainSQL_Failure, ParameterizedSQL_Success, ParameterizedSQL_Failure...} 
TableIdentifier        : MyAuditTableName
FullAuditLogsTableName : SQLDBAuditLogsMyAuditTableName
ResourceGroupName      : resourcegroup01
ServerName             : server01
AuditType              : Table
AuditState             : Enabled
StorageAccountName     : mystorage
StorageKeyType         : Primary
RetentionInDays        : 0
```

### <span data-ttu-id="b2c8d-111">Örnek 2: blob denetimi tanımlanmış bir Azure SQL Server denetim ilkesini alma</span><span class="sxs-lookup"><span data-stu-id="b2c8d-111">Example 2: Get the auditing policy of an Azure SQL server with Blob auditing defined on it</span></span>
```
PS C:\>Get-AzureRmSqlServerAuditingPolicy -ResourceGroupName "resourcegroup01" -ServerName "server01"
AuditActionGroup       : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                          BATCH_COMPLETED_GROUP, ...} 
ResourceGroupName      : resourcegroup01
ServerName             : server01
AuditType              : Blob
AuditState             : Enabled
StorageAccountName     : mystorage
StorageKeyType         : Primary
RetentionInDays        : 0
```

## <span data-ttu-id="b2c8d-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b2c8d-112">PARAMETERS</span></span>

### <span data-ttu-id="b2c8d-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2c8d-113">-ResourceGroupName</span></span>
<span data-ttu-id="b2c8d-114">Azure SQL Server 'ın atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b2c8d-114">Specifies the name of the resource group to which the Azure SQL server is assigned.</span></span>

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

### <span data-ttu-id="b2c8d-115">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b2c8d-115">-ServerName</span></span>
<span data-ttu-id="b2c8d-116">Bu cmdlet 'in denetim ilkesini aldığı Azure SQL Server 'ın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b2c8d-116">Specifies the name of the Azure SQL server for which this cmdlet gets the auditing policy.</span></span>

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

### <span data-ttu-id="b2c8d-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="b2c8d-117">-Confirm</span></span>
<span data-ttu-id="b2c8d-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b2c8d-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b2c8d-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b2c8d-119">-WhatIf</span></span>
<span data-ttu-id="b2c8d-120">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b2c8d-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b2c8d-121">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b2c8d-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b2c8d-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2c8d-122">-DefaultProfile</span></span>
<span data-ttu-id="b2c8d-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b2c8d-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b2c8d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2c8d-124">CommonParameters</span></span>
<span data-ttu-id="b2c8d-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b2c8d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2c8d-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2c8d-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2c8d-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b2c8d-127">INPUTS</span></span>

## <span data-ttu-id="b2c8d-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b2c8d-128">OUTPUTS</span></span>

### <span data-ttu-id="b2c8d-129">Microsoft. Azure. Commands. Sql. Security. model. ServerAuditingPolicyModel</span><span class="sxs-lookup"><span data-stu-id="b2c8d-129">Microsoft.Azure.Commands.Sql.Security.Model.ServerAuditingPolicyModel</span></span>

## <span data-ttu-id="b2c8d-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b2c8d-130">NOTES</span></span>

## <span data-ttu-id="b2c8d-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b2c8d-131">RELATED LINKS</span></span>

[<span data-ttu-id="b2c8d-132">Set-AzureRmSqlServerAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="b2c8d-132">Set-AzureRmSqlServerAuditingPolicy</span></span>](./Set-AzureRmSqlServerAuditingPolicy.md)

[<span data-ttu-id="b2c8d-133">Use-AzureRmSqlServerAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="b2c8d-133">Use-AzureRmSqlServerAuditingPolicy</span></span>](./Use-AzureRmSqlServerAuditingPolicy.md)

[<span data-ttu-id="b2c8d-134">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="b2c8d-134">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


