---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 381F5B34-983C-4733-B384-35D6579B79A2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/use-azurermsqlserverauditingpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Use-AzureRmSqlServerAuditingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Use-AzureRmSqlServerAuditingPolicy.md
ms.openlocfilehash: f74abc2daab0c79c9d070d206a82b33fb15f23f3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592866"
---
# <span data-ttu-id="d7125-101">Use-AzureRmSqlServerAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="d7125-101">Use-AzureRmSqlServerAuditingPolicy</span></span>

## <span data-ttu-id="d7125-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d7125-102">SYNOPSIS</span></span>
<span data-ttu-id="d7125-103">Veritabanının, ana sunucunun Denetim ilkesini kullanacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d7125-103">Specifies that a database uses the auditing policy of its host server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d7125-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d7125-104">SYNTAX</span></span>

```
Use-AzureRmSqlServerAuditingPolicy [-PassThru] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d7125-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d7125-105">DESCRIPTION</span></span>
<span data-ttu-id="d7125-106">**Use-AzureRmSqlServerAuditingPolicy** cmdlet 'i, bir veritabanının ana sunucunun Denetim ilkesini kullandığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d7125-106">The **Use-AzureRmSqlServerAuditingPolicy** cmdlet specifies that a database uses the auditing policy of its host server.</span></span>
<span data-ttu-id="d7125-107">Veritabanını tanımlamak için *Resourcegroupname* , *ServerName* ve *DatabaseName* parametrelerini belirtin.</span><span class="sxs-lookup"><span data-stu-id="d7125-107">Specify the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="d7125-108">Veritabanı sunucusu için denetim ilkesi tanımlanmamışsa, bu cmdlet başarısız olur.</span><span class="sxs-lookup"><span data-stu-id="d7125-108">If no auditing policy is defined for the database server, this cmdlet fails.</span></span>

<span data-ttu-id="d7125-109">Ana bilgisayar sunucu düzeyinde denetim kullanıyorsa, tehdit algılama kaldırılır.</span><span class="sxs-lookup"><span data-stu-id="d7125-109">If the host uses server level auditing, threat detection is removed.</span></span>

## <span data-ttu-id="d7125-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d7125-110">EXAMPLES</span></span>

### <span data-ttu-id="d7125-111">Örnek 1: sunucunun Denetim ilkesini kullanacak şekilde veritabanını yapılandırma</span><span class="sxs-lookup"><span data-stu-id="d7125-111">Example 1: Configure a database to use the auditing policy of its server</span></span>
```
PS C:\>Use-AzureRmSqlServerAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server02" -DatabaseName "Database01"
```

<span data-ttu-id="d7125-112">Bu komut, Database01 adındaki veritabanını, sunucunun Denetim ilkesini kullandığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d7125-112">This command specifies that the database named Database01 on Server02 uses the auditing policy of the server.</span></span>

## <span data-ttu-id="d7125-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d7125-113">PARAMETERS</span></span>

### <span data-ttu-id="d7125-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d7125-114">-DatabaseName</span></span>
<span data-ttu-id="d7125-115">Denetim ilkesini kullanacak veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d7125-115">Specifies the name of the database that will use the auditing policy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7125-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7125-116">-DefaultProfile</span></span>
<span data-ttu-id="d7125-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="d7125-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7125-118">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="d7125-118">-PassThru</span></span>
<span data-ttu-id="d7125-119">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="d7125-119">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="d7125-120">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="d7125-120">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7125-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7125-121">-ResourceGroupName</span></span>
<span data-ttu-id="d7125-122">Sunucunun atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d7125-122">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="d7125-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d7125-123">-ServerName</span></span>
<span data-ttu-id="d7125-124">Denetim ilkesini kullanan veritabanını barındıran sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d7125-124">Specifies the name of the server that hosts the database that uses the auditing policy.</span></span>

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

### <span data-ttu-id="d7125-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7125-125">CommonParameters</span></span>
<span data-ttu-id="d7125-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d7125-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7125-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7125-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7125-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d7125-128">INPUTS</span></span>

### <span data-ttu-id="d7125-129">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="d7125-129">None</span></span>
<span data-ttu-id="d7125-130">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="d7125-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d7125-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d7125-131">OUTPUTS</span></span>

### <span data-ttu-id="d7125-132">Microsoft. Azure. Commands. Sql. Security. model. DatabaseAuditingPolicyModel</span><span class="sxs-lookup"><span data-stu-id="d7125-132">Microsoft.Azure.Commands.Sql.Security.Model.DatabaseAuditingPolicyModel</span></span>

## <span data-ttu-id="d7125-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d7125-133">NOTES</span></span>

## <span data-ttu-id="d7125-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d7125-134">RELATED LINKS</span></span>

[<span data-ttu-id="d7125-135">Get-AzureRmSqlDatabaseAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="d7125-135">Get-AzureRmSqlDatabaseAuditingPolicy</span></span>](./Get-AzureRmSqlDatabaseAuditingPolicy.md)

[<span data-ttu-id="d7125-136">Get-AzureRmSqlServerAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="d7125-136">Get-AzureRmSqlServerAuditingPolicy</span></span>](./Get-AzureRmSqlServerAuditingPolicy.md)

[<span data-ttu-id="d7125-137">Set-AzureRmSqlDatabaseAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="d7125-137">Set-AzureRmSqlDatabaseAuditingPolicy</span></span>](./Set-AzureRmSqlDatabaseAuditingPolicy.md)

[<span data-ttu-id="d7125-138">Set-AzureRmSqlServerAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="d7125-138">Set-AzureRmSqlServerAuditingPolicy</span></span>](./Set-AzureRmSqlServerAuditingPolicy.md)

[<span data-ttu-id="d7125-139">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="d7125-139">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


