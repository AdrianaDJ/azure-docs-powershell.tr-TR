---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 6723557D-8052-4BFA-872C-384B1423B3AE
online version: ''
schema: 2.0.0
ms.openlocfilehash: 185ad06375fe9bbd11cb25c26b25704baeaa1dfe
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105570"
---
# <span data-ttu-id="733a6-101">Get-AzureSqlDatabaseServerQuota</span><span class="sxs-lookup"><span data-stu-id="733a6-101">Get-AzureSqlDatabaseServerQuota</span></span>

## <span data-ttu-id="733a6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="733a6-102">SYNOPSIS</span></span>
<span data-ttu-id="733a6-103">Bir Azure SQL veritabanı sunucusu için kota bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="733a6-103">Gets quota information for an Azure SQL Database server.</span></span>

## <span data-ttu-id="733a6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="733a6-104">SYNTAX</span></span>

### <span data-ttu-id="733a6-105">ByConnectionContext</span><span class="sxs-lookup"><span data-stu-id="733a6-105">ByConnectionContext</span></span>
```
Get-AzureSqlDatabaseServerQuota -ConnectionContext <IServerDataServiceContext> [-QuotaName <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="733a6-106">ByServerName</span><span class="sxs-lookup"><span data-stu-id="733a6-106">ByServerName</span></span>
```
Get-AzureSqlDatabaseServerQuota -ServerName <String> [-QuotaName <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="733a6-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="733a6-107">DESCRIPTION</span></span>
<span data-ttu-id="733a6-108">**Get-Azuressqldatabaseserverquota** cmdlet 'i, belirli BIR Azure SQL veritabanı sunucusu örneğinin kota bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="733a6-108">The **Get-AzureSqlDatabaseServerQuota** cmdlet gets the quota information for a specified instance of Azure SQL Database Server.</span></span>
<span data-ttu-id="733a6-109">Bir bağlantı bağlamı veya sunucu adı belirtin.</span><span class="sxs-lookup"><span data-stu-id="733a6-109">Specify a connection context or the server name.</span></span>
<span data-ttu-id="733a6-110">Kota adı belirtmezseniz, bu cmdlet sunucunun tüm kota bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="733a6-110">If you do not specify a quota name, this cmdlet gets all the quota information for the server.</span></span>

## <span data-ttu-id="733a6-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="733a6-111">EXAMPLES</span></span>

### <span data-ttu-id="733a6-112">Örnek 1: belirli bir kotanın bilgilerini alma</span><span class="sxs-lookup"><span data-stu-id="733a6-112">Example 1: Get information for a specific quota</span></span>
```
PS C:\> $QuotaPremium = GetAzureSqlDatabaseServerQuota $Context -QuotaName "Premium_Databases"
```

<span data-ttu-id="733a6-113">Bu komut Premium_Databases adlı kotayı, $Context değişkeninde depolanan bağlantının belirttiği Azure SQL veritabanı sunucusundan alır.</span><span class="sxs-lookup"><span data-stu-id="733a6-113">This command gets the quota named Premium_Databases from the Azure SQL Database server specified by the connection stored in the $Context variable.</span></span>

### <span data-ttu-id="733a6-114">Örnek 2: tüm kotalar için bilgi alma</span><span class="sxs-lookup"><span data-stu-id="733a6-114">Example 2: Get information for all quotas</span></span>
```
PS C:\> $QuotaList = GetAzureSqlDatabaseServerQuota $Context
```

<span data-ttu-id="733a6-115">Bu komut, bağlantı $Context belirtilen sunucudan tüm kota değerlerini alır.</span><span class="sxs-lookup"><span data-stu-id="733a6-115">This command gets all quota values from the server specified by the connection $Context.</span></span>

## <span data-ttu-id="733a6-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="733a6-116">PARAMETERS</span></span>

### <span data-ttu-id="733a6-117">-ConnectionContext</span><span class="sxs-lookup"><span data-stu-id="733a6-117">-ConnectionContext</span></span>
<span data-ttu-id="733a6-118">Sunucunun bağlantı bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="733a6-118">Specifies the connection context of a server.</span></span>

```yaml
Type: IServerDataServiceContext
Parameter Sets: ByConnectionContext
Aliases: Context

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="733a6-119">-Profil</span><span class="sxs-lookup"><span data-stu-id="733a6-119">-Profile</span></span>
<span data-ttu-id="733a6-120">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="733a6-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="733a6-121">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="733a6-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="733a6-122">-Tırnak işareti</span><span class="sxs-lookup"><span data-stu-id="733a6-122">-QuotaName</span></span>
<span data-ttu-id="733a6-123">Bu cmdlet 'in aldığı kota değerinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="733a6-123">Specifies the name of the quota value that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="733a6-124">-ServerName</span><span class="sxs-lookup"><span data-stu-id="733a6-124">-ServerName</span></span>
<span data-ttu-id="733a6-125">Sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="733a6-125">Specifies the name of a server.</span></span>

```yaml
Type: String
Parameter Sets: ByServerName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="733a6-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="733a6-126">CommonParameters</span></span>
<span data-ttu-id="733a6-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="733a6-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="733a6-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="733a6-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="733a6-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="733a6-129">INPUTS</span></span>

## <span data-ttu-id="733a6-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="733a6-130">OUTPUTS</span></span>

### <span data-ttu-id="733a6-131">Microsoft. Windowsazde. Commands. SqlDatabase. Services. Server. Sunucuquota []</span><span class="sxs-lookup"><span data-stu-id="733a6-131">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.ServerQuota[]</span></span>

## <span data-ttu-id="733a6-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="733a6-132">NOTES</span></span>
* <span data-ttu-id="733a6-133">Kimlik doğrulama: Bu cmdlet SQL Server kimlik doğrulaması veya sertifika tabanlı kimlik doğrulaması kullanabilir.</span><span class="sxs-lookup"><span data-stu-id="733a6-133">Authentication: This cmdlet can use either SQL Server authentication or certificate-based authentication.</span></span> <span data-ttu-id="733a6-134">Kimlik doğrulamasını ayarlama örnekleri için New-AzureSqlDatabaseServerContext cmdlet 'ine bakın.</span><span class="sxs-lookup"><span data-stu-id="733a6-134">For examples of setting up authentication, see the New-AzureSqlDatabaseServerContext cmdlet.</span></span>

## <span data-ttu-id="733a6-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="733a6-135">RELATED LINKS</span></span>

[<span data-ttu-id="733a6-136">Azure SQL veritabanı</span><span class="sxs-lookup"><span data-stu-id="733a6-136">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="733a6-137">Azure SQL veritabanları için işlemler</span><span class="sxs-lookup"><span data-stu-id="733a6-137">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="733a6-138">New-Azuressqldatabaseservercontext</span><span class="sxs-lookup"><span data-stu-id="733a6-138">New-AzureSqlDatabaseServerContext</span></span>](./New-AzureSqlDatabaseServerContext.md)


