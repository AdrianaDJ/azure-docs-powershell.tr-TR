---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 0ACEDE22-1C2B-4846-A949-710AF6C148D0
online version: ''
schema: 2.0.0
ms.openlocfilehash: d513d6d019c84984923541624063e657e2250b61
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105571"
---
# <span data-ttu-id="702fb-101">Get-AzureSqlDatabaseServer</span><span class="sxs-lookup"><span data-stu-id="702fb-101">Get-AzureSqlDatabaseServer</span></span>

## <span data-ttu-id="702fb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="702fb-102">SYNOPSIS</span></span>
<span data-ttu-id="702fb-103">Azure SQL veritabanı sunucuları hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="702fb-103">Gets information about Azure SQL Database servers.</span></span>

## <span data-ttu-id="702fb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="702fb-104">SYNTAX</span></span>

```
Get-AzureSqlDatabaseServer [-ServerName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="702fb-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="702fb-105">DESCRIPTION</span></span>
<span data-ttu-id="702fb-106">**Get-Azuressqldatabaseserver** cmdlet 'i, geçerli ABONELIKTEKI Azure SQL veritabanı sunucusu örnekleri hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="702fb-106">The **Get-AzureSqlDatabaseServer** cmdlet gets information about the instances of Azure SQL Database Server in the current subscription.</span></span>
<span data-ttu-id="702fb-107">Bir sunucuyu adıyla belirtirseniz, bu cmdlet bu sunucu hakkında bilgi içeren bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="702fb-107">If you specify a server by name, this cmdlet returns an object that contains information about that server.</span></span>
<span data-ttu-id="702fb-108">Aksi halde cmdlet, tüm sunucular hakkında bilgi döndürür.</span><span class="sxs-lookup"><span data-stu-id="702fb-108">Otherwise, the cmdlet returns information about all the servers.</span></span>

## <span data-ttu-id="702fb-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="702fb-109">EXAMPLES</span></span>

### <span data-ttu-id="702fb-110">Örnek 1: tüm sunucular hakkında bilgi edinme</span><span class="sxs-lookup"><span data-stu-id="702fb-110">Example 1: Get information about all servers</span></span>
```
PS C:\> Get-AzureSqlDatabaseServer
```

<span data-ttu-id="702fb-111">Bu komut, geçerli abonelikteki tüm Azure SQL veritabanı sunucusu örnekleri hakkında bilgi döndürür.</span><span class="sxs-lookup"><span data-stu-id="702fb-111">This command returns information about all instances of Azure SQL Database Server in the current subscription.</span></span>

### <span data-ttu-id="702fb-112">Örnek 2: belirli bir sunucu hakkında bilgi alma</span><span class="sxs-lookup"><span data-stu-id="702fb-112">Example 2: Get information about a specific server</span></span>
```
PS C:\> Get-AzureSqlDatabaseServer -ServerName "lpqd0zbr8y"
```

<span data-ttu-id="702fb-113">Bu komut, lpqd0zbr8y adlı sunucu hakkındaki bilgileri döndürür.</span><span class="sxs-lookup"><span data-stu-id="702fb-113">This command returns information about the server named lpqd0zbr8y.</span></span>

## <span data-ttu-id="702fb-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="702fb-114">PARAMETERS</span></span>

### <span data-ttu-id="702fb-115">-Profil</span><span class="sxs-lookup"><span data-stu-id="702fb-115">-Profile</span></span>
<span data-ttu-id="702fb-116">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="702fb-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="702fb-117">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="702fb-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="702fb-118">-ServerName</span><span class="sxs-lookup"><span data-stu-id="702fb-118">-ServerName</span></span>
<span data-ttu-id="702fb-119">Bu cmdlet 'in kaldırdığı sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="702fb-119">Specifies the name of the server that this cmdlet removes.</span></span>
<span data-ttu-id="702fb-120">Tam DNS adını değil, sunucu adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="702fb-120">Specify the server name, not the fully qualified DNS name.</span></span>

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

### <span data-ttu-id="702fb-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="702fb-121">CommonParameters</span></span>
<span data-ttu-id="702fb-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="702fb-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="702fb-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="702fb-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="702fb-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="702fb-124">INPUTS</span></span>

### <span data-ttu-id="702fb-125">Microsoft. Windowsazve. Commands. SqlDatabase. model. SqlDatabaseServerContext</span><span class="sxs-lookup"><span data-stu-id="702fb-125">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.SqlDatabaseServerContext</span></span>

## <span data-ttu-id="702fb-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="702fb-126">OUTPUTS</span></span>

### <span data-ttu-id="702fb-127">'A\<Microsoft.WindowsAzure.Commands.SqlDatabase.Model.SqlDatabaseServerContext\></span><span class="sxs-lookup"><span data-stu-id="702fb-127">IEnumerable\<Microsoft.WindowsAzure.Commands.SqlDatabase.Model.SqlDatabaseServerContext\></span></span>

## <span data-ttu-id="702fb-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="702fb-128">NOTES</span></span>

## <span data-ttu-id="702fb-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="702fb-129">RELATED LINKS</span></span>

[<span data-ttu-id="702fb-130">Azure SQL veritabanı</span><span class="sxs-lookup"><span data-stu-id="702fb-130">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="702fb-131">Liste sunucuları</span><span class="sxs-lookup"><span data-stu-id="702fb-131">List Servers</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505702.aspx)

[<span data-ttu-id="702fb-132">Azure SQL veritabanları için işlemler</span><span class="sxs-lookup"><span data-stu-id="702fb-132">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="702fb-133">New-Azuressqldatabaseserver</span><span class="sxs-lookup"><span data-stu-id="702fb-133">New-AzureSqlDatabaseServer</span></span>](./New-AzureSqlDatabaseServer.md)

[<span data-ttu-id="702fb-134">Remove-Azuressqldatabaseserver</span><span class="sxs-lookup"><span data-stu-id="702fb-134">Remove-AzureSqlDatabaseServer</span></span>](./Remove-AzureSqlDatabaseServer.md)

[<span data-ttu-id="702fb-135">Set-Azuressqldatabaseserver</span><span class="sxs-lookup"><span data-stu-id="702fb-135">Set-AzureSqlDatabaseServer</span></span>](./Set-AzureSqlDatabaseServer.md)


