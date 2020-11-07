---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: 22ACB910-0C41-4649-8D22-537E38CB4570
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/new-Azwebappdatabasebackupsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/New-AzWebAppDatabaseBackupSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/New-AzWebAppDatabaseBackupSetting.md
ms.openlocfilehash: 7ea02fb05c64c751fc339c889098724b2822a8b8
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936088"
---
# <span data-ttu-id="ec9ab-101">New-AzWebAppDatabaseBackupSetting</span><span class="sxs-lookup"><span data-stu-id="ec9ab-101">New-AzWebAppDatabaseBackupSetting</span></span>

## <span data-ttu-id="ec9ab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ec9ab-102">SYNOPSIS</span></span>

## <span data-ttu-id="ec9ab-103">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ec9ab-103">SYNTAX</span></span>

```
New-AzWebAppDatabaseBackupSetting [-Name] <String> [-DatabaseType] <String> [-ConnectionString] <String>
 [[-ConnectionStringName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ec9ab-104">Tanım</span><span class="sxs-lookup"><span data-stu-id="ec9ab-104">DESCRIPTION</span></span>
<span data-ttu-id="ec9ab-105">**New-AzWebAppDatabaseBackupSetting** cmdlet 'i yeni bir Azure Web App yedekleme ayarı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ec9ab-105">The **New-AzWebAppDatabaseBackupSetting** cmdlet creates a new Azure Web App Backup setting.</span></span>

## <span data-ttu-id="ec9ab-106">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ec9ab-106">EXAMPLES</span></span>

### <span data-ttu-id="ec9ab-107">2</span><span class="sxs-lookup"><span data-stu-id="ec9ab-107">1:</span></span>
```
PS C:\> New-AzWebAppDatabaseBackupSetting -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -ConnectionString "MyConnectionString" -DatabaseType "SqlAzure"
```

<span data-ttu-id="ec9ab-108">Varsayılan-Web-WestUS kaynak grubundaki belirtilen uygulama ContosoWebApp için SqlAzure türünde bir veritabanı yedekleme ayarı (bağlantı dizesi) oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ec9ab-108">Creates a database backup setting (connection string) of type SqlAzure for the specified app ContosoWebApp that is within resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="ec9ab-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ec9ab-109">PARAMETERS</span></span>

### <span data-ttu-id="ec9ab-110">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="ec9ab-110">-ConnectionString</span></span>
<span data-ttu-id="ec9ab-111">Bağlantı dizesi</span><span class="sxs-lookup"><span data-stu-id="ec9ab-111">Connection String</span></span>

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

### <span data-ttu-id="ec9ab-112">-ConnectionStringName</span><span class="sxs-lookup"><span data-stu-id="ec9ab-112">-ConnectionStringName</span></span>
<span data-ttu-id="ec9ab-113">Bağlantı dizesi adı</span><span class="sxs-lookup"><span data-stu-id="ec9ab-113">Connection String Name</span></span>

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

### <span data-ttu-id="ec9ab-114">-DatabaseType</span><span class="sxs-lookup"><span data-stu-id="ec9ab-114">-DatabaseType</span></span>
<span data-ttu-id="ec9ab-115">Veritabanı türü (örneğin, "SqlAzure" veya "MySql")</span><span class="sxs-lookup"><span data-stu-id="ec9ab-115">Database Type ( e.g. "SqlAzure" or "MySql" )</span></span>

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

### <span data-ttu-id="ec9ab-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec9ab-116">-DefaultProfile</span></span>
<span data-ttu-id="ec9ab-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ec9ab-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec9ab-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="ec9ab-118">-Name</span></span>
<span data-ttu-id="ec9ab-119">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="ec9ab-119">WebApp Name</span></span>

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

### <span data-ttu-id="ec9ab-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec9ab-120">CommonParameters</span></span>
<span data-ttu-id="ec9ab-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ec9ab-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec9ab-122">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ec9ab-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec9ab-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ec9ab-123">INPUTS</span></span>

### <span data-ttu-id="ec9ab-124">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="ec9ab-124">None</span></span>
<span data-ttu-id="ec9ab-125">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="ec9ab-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ec9ab-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ec9ab-126">OUTPUTS</span></span>

### <span data-ttu-id="ec9ab-127">Microsoft. Azure. Management. Web sitesi. modeller. DatabaseBackupSetting</span><span class="sxs-lookup"><span data-stu-id="ec9ab-127">Microsoft.Azure.Management.WebSites.Models.DatabaseBackupSetting</span></span>

## <span data-ttu-id="ec9ab-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ec9ab-128">NOTES</span></span>

## <span data-ttu-id="ec9ab-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ec9ab-129">RELATED LINKS</span></span>

