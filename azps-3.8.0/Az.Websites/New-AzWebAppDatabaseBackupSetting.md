---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 22ACB910-0C41-4649-8D22-537E38CB4570
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/new-azwebappdatabasebackupsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppDatabaseBackupSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppDatabaseBackupSetting.md
ms.openlocfilehash: 480532e2fffcc2b03a57c7d0a63cc2737844f652
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096211"
---
# <span data-ttu-id="747a0-101">New-AzWebAppDatabaseBackupSetting</span><span class="sxs-lookup"><span data-stu-id="747a0-101">New-AzWebAppDatabaseBackupSetting</span></span>

## <span data-ttu-id="747a0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="747a0-102">SYNOPSIS</span></span>

## <span data-ttu-id="747a0-103">INDEKI</span><span class="sxs-lookup"><span data-stu-id="747a0-103">SYNTAX</span></span>

```
New-AzWebAppDatabaseBackupSetting [-Name] <String> [-DatabaseType] <String> [-ConnectionString] <String>
 [[-ConnectionStringName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="747a0-104">Tanım</span><span class="sxs-lookup"><span data-stu-id="747a0-104">DESCRIPTION</span></span>
<span data-ttu-id="747a0-105">**New-AzWebAppDatabaseBackupSetting** cmdlet 'i yeni bir Azure Web App yedekleme ayarı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="747a0-105">The **New-AzWebAppDatabaseBackupSetting** cmdlet creates a new Azure Web App Backup setting.</span></span>

## <span data-ttu-id="747a0-106">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="747a0-106">EXAMPLES</span></span>

### <span data-ttu-id="747a0-107">2</span><span class="sxs-lookup"><span data-stu-id="747a0-107">1:</span></span>
```
PS C:\> New-AzWebAppDatabaseBackupSetting -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -ConnectionString "MyConnectionString" -DatabaseType "SqlAzure"
```

<span data-ttu-id="747a0-108">Varsayılan-Web-WestUS kaynak grubundaki belirtilen uygulama ContosoWebApp için SqlAzure türünde bir veritabanı yedekleme ayarı (bağlantı dizesi) oluşturur.</span><span class="sxs-lookup"><span data-stu-id="747a0-108">Creates a database backup setting (connection string) of type SqlAzure for the specified app ContosoWebApp that is within resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="747a0-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="747a0-109">PARAMETERS</span></span>

### <span data-ttu-id="747a0-110">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="747a0-110">-ConnectionString</span></span>
<span data-ttu-id="747a0-111">Bağlantı dizesi</span><span class="sxs-lookup"><span data-stu-id="747a0-111">Connection String</span></span>

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

### <span data-ttu-id="747a0-112">-ConnectionStringName</span><span class="sxs-lookup"><span data-stu-id="747a0-112">-ConnectionStringName</span></span>
<span data-ttu-id="747a0-113">Bağlantı dizesi adı</span><span class="sxs-lookup"><span data-stu-id="747a0-113">Connection String Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="747a0-114">-DatabaseType</span><span class="sxs-lookup"><span data-stu-id="747a0-114">-DatabaseType</span></span>
<span data-ttu-id="747a0-115">Veritabanı türü (örneğin, "SqlAzure" veya "MySql")</span><span class="sxs-lookup"><span data-stu-id="747a0-115">Database Type ( e.g. "SqlAzure" or "MySql" )</span></span>

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

### <span data-ttu-id="747a0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="747a0-116">-DefaultProfile</span></span>
<span data-ttu-id="747a0-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="747a0-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="747a0-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="747a0-118">-Name</span></span>
<span data-ttu-id="747a0-119">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="747a0-119">WebApp Name</span></span>

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

### <span data-ttu-id="747a0-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="747a0-120">CommonParameters</span></span>
<span data-ttu-id="747a0-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="747a0-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="747a0-122">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="747a0-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="747a0-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="747a0-123">INPUTS</span></span>

### <span data-ttu-id="747a0-124">System. String</span><span class="sxs-lookup"><span data-stu-id="747a0-124">System.String</span></span>

## <span data-ttu-id="747a0-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="747a0-125">OUTPUTS</span></span>

### <span data-ttu-id="747a0-126">Microsoft. Azure. Management. Web sitesi. modeller. DatabaseBackupSetting</span><span class="sxs-lookup"><span data-stu-id="747a0-126">Microsoft.Azure.Management.WebSites.Models.DatabaseBackupSetting</span></span>

## <span data-ttu-id="747a0-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="747a0-127">NOTES</span></span>

## <span data-ttu-id="747a0-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="747a0-128">RELATED LINKS</span></span>
