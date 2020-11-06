---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 381F5B34-983C-4733-B384-35D6579B79A2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Use-AzureRmSqlServerAuditingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Use-AzureRmSqlServerAuditingPolicy.md
ms.openlocfilehash: 9e3e94109904bc14f22e2ca2c08936316ed597db
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592165"
---
# <span data-ttu-id="474a6-101">Use-AzureRmSqlServerAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="474a6-101">Use-AzureRmSqlServerAuditingPolicy</span></span>

## <span data-ttu-id="474a6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="474a6-102">SYNOPSIS</span></span>
<span data-ttu-id="474a6-103">Veritabanının, ana sunucunun Denetim ilkesini kullanacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="474a6-103">Specifies that a database uses the auditing policy of its host server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="474a6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="474a6-104">SYNTAX</span></span>

```
Use-AzureRmSqlServerAuditingPolicy [-PassThru] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="474a6-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="474a6-105">DESCRIPTION</span></span>
<span data-ttu-id="474a6-106">**Use-AzureRmSqlServerAuditingPolicy** cmdlet 'i, bir veritabanının ana sunucunun Denetim ilkesini kullandığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="474a6-106">The **Use-AzureRmSqlServerAuditingPolicy** cmdlet specifies that a database uses the auditing policy of its host server.</span></span>
<span data-ttu-id="474a6-107">Veritabanını tanımlamak için *Resourcegroupname* , *ServerName* ve *DatabaseName* parametrelerini belirtin.</span><span class="sxs-lookup"><span data-stu-id="474a6-107">Specify the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="474a6-108">Veritabanı sunucusu için denetim ilkesi tanımlanmamışsa, bu cmdlet başarısız olur.</span><span class="sxs-lookup"><span data-stu-id="474a6-108">If no auditing policy is defined for the database server, this cmdlet fails.</span></span>

<span data-ttu-id="474a6-109">Ana bilgisayar sunucu düzeyinde denetim kullanıyorsa, tehdit algılama kaldırılır.</span><span class="sxs-lookup"><span data-stu-id="474a6-109">If the host uses server level auditing, threat detection is removed.</span></span>

## <span data-ttu-id="474a6-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="474a6-110">EXAMPLES</span></span>

### <span data-ttu-id="474a6-111">Örnek 1: sunucunun Denetim ilkesini kullanacak şekilde veritabanını yapılandırma</span><span class="sxs-lookup"><span data-stu-id="474a6-111">Example 1: Configure a database to use the auditing policy of its server</span></span>
```
PS C:\>Use-AzureRmSqlServerAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server02" -DatabaseName "Database01"
```

<span data-ttu-id="474a6-112">Bu komut, Database01 adındaki veritabanını, sunucunun Denetim ilkesini kullandığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="474a6-112">This command specifies that the database named Database01 on Server02 uses the auditing policy of the server.</span></span>

## <span data-ttu-id="474a6-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="474a6-113">PARAMETERS</span></span>

### <span data-ttu-id="474a6-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="474a6-114">-DatabaseName</span></span>
<span data-ttu-id="474a6-115">Denetim ilkesini kullanacak veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="474a6-115">Specifies the name of the database that will use the auditing policy.</span></span>

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

### <span data-ttu-id="474a6-116">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="474a6-116">-PassThru</span></span>
<span data-ttu-id="474a6-117">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="474a6-117">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="474a6-118">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="474a6-118">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="474a6-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="474a6-119">-ResourceGroupName</span></span>
<span data-ttu-id="474a6-120">Sunucunun atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="474a6-120">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="474a6-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="474a6-121">-ServerName</span></span>
<span data-ttu-id="474a6-122">Denetim ilkesini kullanan veritabanını barındıran sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="474a6-122">Specifies the name of the server that hosts the database that uses the auditing policy.</span></span>

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

### <span data-ttu-id="474a6-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="474a6-123">-DefaultProfile</span></span>
<span data-ttu-id="474a6-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="474a6-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="474a6-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="474a6-125">CommonParameters</span></span>
<span data-ttu-id="474a6-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="474a6-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="474a6-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="474a6-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="474a6-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="474a6-128">INPUTS</span></span>

## <span data-ttu-id="474a6-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="474a6-129">OUTPUTS</span></span>

### <span data-ttu-id="474a6-130">Microsoft. Azure. Commands. Sql. Security. model. DatabaseAuditingPolicyModel</span><span class="sxs-lookup"><span data-stu-id="474a6-130">Microsoft.Azure.Commands.Sql.Security.Model.DatabaseAuditingPolicyModel</span></span>

## <span data-ttu-id="474a6-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="474a6-131">NOTES</span></span>

## <span data-ttu-id="474a6-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="474a6-132">RELATED LINKS</span></span>

[<span data-ttu-id="474a6-133">Get-AzureRmSqlDatabaseAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="474a6-133">Get-AzureRmSqlDatabaseAuditingPolicy</span></span>](./Get-AzureRmSqlDatabaseAuditingPolicy.md)

[<span data-ttu-id="474a6-134">Get-AzureRmSqlServerAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="474a6-134">Get-AzureRmSqlServerAuditingPolicy</span></span>](./Get-AzureRmSqlServerAuditingPolicy.md)

[<span data-ttu-id="474a6-135">Set-AzureRmSqlDatabaseAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="474a6-135">Set-AzureRmSqlDatabaseAuditingPolicy</span></span>](./Set-AzureRmSqlDatabaseAuditingPolicy.md)

[<span data-ttu-id="474a6-136">Set-AzureRmSqlServerAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="474a6-136">Set-AzureRmSqlServerAuditingPolicy</span></span>](./Set-AzureRmSqlServerAuditingPolicy.md)

[<span data-ttu-id="474a6-137">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="474a6-137">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


