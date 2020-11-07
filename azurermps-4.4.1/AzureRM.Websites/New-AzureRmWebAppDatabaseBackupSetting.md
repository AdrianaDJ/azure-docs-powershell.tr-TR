---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 22ACB910-0C41-4649-8D22-537E38CB4570
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebAppDatabaseBackupSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebAppDatabaseBackupSetting.md
ms.openlocfilehash: d8662f0a3f9ff10fccd9d38a2d5397bf32ea6b8a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764745"
---
# <span data-ttu-id="136ad-101">New-AzureRmWebAppDatabaseBackupSetting</span><span class="sxs-lookup"><span data-stu-id="136ad-101">New-AzureRmWebAppDatabaseBackupSetting</span></span>

## <span data-ttu-id="136ad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="136ad-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="136ad-103">INDEKI</span><span class="sxs-lookup"><span data-stu-id="136ad-103">SYNTAX</span></span>

```
New-AzureRmWebAppDatabaseBackupSetting [-Name] <String> [-DatabaseType] <String> [-ConnectionString] <String>
 [[-ConnectionStringName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="136ad-104">Tanım</span><span class="sxs-lookup"><span data-stu-id="136ad-104">DESCRIPTION</span></span>
<span data-ttu-id="136ad-105">**New-AzureRmWebAppDatabaseBackupSetting** cmdlet 'i, yeni bir Azure Web App yedekleme ayarı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="136ad-105">The **New-AzureRmWebAppDatabaseBackupSetting** cmdlet creates a new Azure Web App Backup setting.</span></span>

## <span data-ttu-id="136ad-106">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="136ad-106">EXAMPLES</span></span>

### <span data-ttu-id="136ad-107">2</span><span class="sxs-lookup"><span data-stu-id="136ad-107">1:</span></span>
```
PS C:\> New-AzureRmWebAppDatabaseBackupSetting -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -ConnectionString "MyConnectionString" -DatabaseType "SqlAzure"
```

<span data-ttu-id="136ad-108">Varsayılan-Web-WestUS kaynak grubundaki belirtilen uygulama ContosoWebApp için SqlAzure türünde bir veritabanı yedekleme ayarı (bağlantı dizesi) oluşturur.</span><span class="sxs-lookup"><span data-stu-id="136ad-108">Creates a database backup setting (connection string) of type SqlAzure for the specified app ContosoWebApp that is within resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="136ad-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="136ad-109">PARAMETERS</span></span>

### <span data-ttu-id="136ad-110">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="136ad-110">-ConnectionString</span></span>
<span data-ttu-id="136ad-111">Bağlantı dizesi</span><span class="sxs-lookup"><span data-stu-id="136ad-111">Connection String</span></span>

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

### <span data-ttu-id="136ad-112">-ConnectionStringName</span><span class="sxs-lookup"><span data-stu-id="136ad-112">-ConnectionStringName</span></span>
<span data-ttu-id="136ad-113">Bağlantı dizesi adı</span><span class="sxs-lookup"><span data-stu-id="136ad-113">Connection String Name</span></span>

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

### <span data-ttu-id="136ad-114">-DatabaseType</span><span class="sxs-lookup"><span data-stu-id="136ad-114">-DatabaseType</span></span>
<span data-ttu-id="136ad-115">Veritabanı türü (örneğin, "SqlAzure" veya "MySql")</span><span class="sxs-lookup"><span data-stu-id="136ad-115">Database Type ( e.g. "SqlAzure" or "MySql" )</span></span>

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

### <span data-ttu-id="136ad-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="136ad-116">-Name</span></span>
<span data-ttu-id="136ad-117">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="136ad-117">WebApp Name</span></span>

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

### <span data-ttu-id="136ad-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="136ad-118">-DefaultProfile</span></span>
<span data-ttu-id="136ad-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="136ad-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="136ad-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="136ad-120">CommonParameters</span></span>
<span data-ttu-id="136ad-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="136ad-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="136ad-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="136ad-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="136ad-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="136ad-123">INPUTS</span></span>

## <span data-ttu-id="136ad-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="136ad-124">OUTPUTS</span></span>

### <span data-ttu-id="136ad-125">Microsoft. Azure. Management. Web sitesi. modeller. DatabaseBackupSetting</span><span class="sxs-lookup"><span data-stu-id="136ad-125">Microsoft.Azure.Management.WebSites.Models.DatabaseBackupSetting</span></span>

## <span data-ttu-id="136ad-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="136ad-126">NOTES</span></span>

## <span data-ttu-id="136ad-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="136ad-127">RELATED LINKS</span></span>

