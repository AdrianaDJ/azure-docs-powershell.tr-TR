---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: 22ACB910-0C41-4649-8D22-537E38CB4570
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/new-azurermwebappdatabasebackupsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebAppDatabaseBackupSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebAppDatabaseBackupSetting.md
ms.openlocfilehash: 7eea25d4b82dc8a424fea0cbd3e361014c77c396
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592361"
---
# <span data-ttu-id="2e0fa-101">New-AzureRmWebAppDatabaseBackupSetting</span><span class="sxs-lookup"><span data-stu-id="2e0fa-101">New-AzureRmWebAppDatabaseBackupSetting</span></span>

## <span data-ttu-id="2e0fa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2e0fa-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2e0fa-103">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2e0fa-103">SYNTAX</span></span>

```
New-AzureRmWebAppDatabaseBackupSetting [-Name] <String> [-DatabaseType] <String> [-ConnectionString] <String>
 [[-ConnectionStringName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2e0fa-104">Tanım</span><span class="sxs-lookup"><span data-stu-id="2e0fa-104">DESCRIPTION</span></span>
<span data-ttu-id="2e0fa-105">**New-AzureRmWebAppDatabaseBackupSetting** cmdlet 'i, yeni bir Azure Web App yedekleme ayarı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2e0fa-105">The **New-AzureRmWebAppDatabaseBackupSetting** cmdlet creates a new Azure Web App Backup setting.</span></span>

## <span data-ttu-id="2e0fa-106">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2e0fa-106">EXAMPLES</span></span>

### <span data-ttu-id="2e0fa-107">2</span><span class="sxs-lookup"><span data-stu-id="2e0fa-107">1:</span></span>
```
PS C:\> New-AzureRmWebAppDatabaseBackupSetting -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -ConnectionString "MyConnectionString" -DatabaseType "SqlAzure"
```

<span data-ttu-id="2e0fa-108">Varsayılan-Web-WestUS kaynak grubundaki belirtilen uygulama ContosoWebApp için SqlAzure türünde bir veritabanı yedekleme ayarı (bağlantı dizesi) oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2e0fa-108">Creates a database backup setting (connection string) of type SqlAzure for the specified app ContosoWebApp that is within resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="2e0fa-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2e0fa-109">PARAMETERS</span></span>

### <span data-ttu-id="2e0fa-110">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="2e0fa-110">-ConnectionString</span></span>
<span data-ttu-id="2e0fa-111">Bağlantı dizesi</span><span class="sxs-lookup"><span data-stu-id="2e0fa-111">Connection String</span></span>

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

### <span data-ttu-id="2e0fa-112">-ConnectionStringName</span><span class="sxs-lookup"><span data-stu-id="2e0fa-112">-ConnectionStringName</span></span>
<span data-ttu-id="2e0fa-113">Bağlantı dizesi adı</span><span class="sxs-lookup"><span data-stu-id="2e0fa-113">Connection String Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e0fa-114">-DatabaseType</span><span class="sxs-lookup"><span data-stu-id="2e0fa-114">-DatabaseType</span></span>
<span data-ttu-id="2e0fa-115">Veritabanı türü (örneğin, "SqlAzure" veya "MySql")</span><span class="sxs-lookup"><span data-stu-id="2e0fa-115">Database Type ( e.g. "SqlAzure" or "MySql" )</span></span>

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

### <span data-ttu-id="2e0fa-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e0fa-116">-DefaultProfile</span></span>
<span data-ttu-id="2e0fa-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2e0fa-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2e0fa-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="2e0fa-118">-Name</span></span>
<span data-ttu-id="2e0fa-119">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="2e0fa-119">WebApp Name</span></span>

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

### <span data-ttu-id="2e0fa-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e0fa-120">CommonParameters</span></span>
<span data-ttu-id="2e0fa-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2e0fa-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e0fa-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e0fa-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e0fa-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2e0fa-123">INPUTS</span></span>

### <span data-ttu-id="2e0fa-124">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="2e0fa-124">None</span></span>
<span data-ttu-id="2e0fa-125">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="2e0fa-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2e0fa-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2e0fa-126">OUTPUTS</span></span>

### <span data-ttu-id="2e0fa-127">Microsoft. Azure. Management. Web sitesi. modeller. DatabaseBackupSetting</span><span class="sxs-lookup"><span data-stu-id="2e0fa-127">Microsoft.Azure.Management.WebSites.Models.DatabaseBackupSetting</span></span>

## <span data-ttu-id="2e0fa-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2e0fa-128">NOTES</span></span>

## <span data-ttu-id="2e0fa-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2e0fa-129">RELATED LINKS</span></span>

