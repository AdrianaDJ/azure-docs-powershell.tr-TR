---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: C0BE6C8D-37F5-445F-AE15-2CD4F8D8E031
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/new-azurermdatalakeanalyticscatalogsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/New-AzureRmDataLakeAnalyticsCatalogSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/New-AzureRmDataLakeAnalyticsCatalogSecret.md
ms.openlocfilehash: ce6bd748a639116f1f6d2e5c42e824fb3687bdfb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593262"
---
# <span data-ttu-id="beaa3-101">New-AzureRmDataLakeAnalyticsCatalogSecret</span><span class="sxs-lookup"><span data-stu-id="beaa3-101">New-AzureRmDataLakeAnalyticsCatalogSecret</span></span>

## <span data-ttu-id="beaa3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="beaa3-102">SYNOPSIS</span></span>
<span data-ttu-id="beaa3-103">Veri Lake Analytics Katalog gizliliğini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="beaa3-103">Creates a Data Lake Analytics catalog secret.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="beaa3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="beaa3-104">SYNTAX</span></span>

### <span data-ttu-id="beaa3-105">CreateByFullURI</span><span class="sxs-lookup"><span data-stu-id="beaa3-105">CreateByFullURI</span></span>
```
New-AzureRmDataLakeAnalyticsCatalogSecret [-Account] <String> [-DatabaseName] <String> [-Secret] <PSCredential>
 [-DatabaseHost] <String> [-Port] <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="beaa3-106">CreateByHostNameAndPort</span><span class="sxs-lookup"><span data-stu-id="beaa3-106">CreateByHostNameAndPort</span></span>
```
New-AzureRmDataLakeAnalyticsCatalogSecret [-Account] <String> [-DatabaseName] <String> [-Secret] <PSCredential>
 [-Uri] <Uri> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="beaa3-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="beaa3-107">DESCRIPTION</span></span>
<span data-ttu-id="beaa3-108">**New-Azurermdatalakeanalyzer Ticdağındağın**</span><span class="sxs-lookup"><span data-stu-id="beaa3-108">The **New-AzureRmDataLakeAnalyticsCatalogSecret** cmdlet creates a secret to use in an Azure Data Lake Analytics catalog.</span></span>

## <span data-ttu-id="beaa3-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="beaa3-109">EXAMPLES</span></span>

### <span data-ttu-id="beaa3-110">Örnek 1: kataloğun gizliliğini alma</span><span class="sxs-lookup"><span data-stu-id="beaa3-110">Example 1: Get the secret for a catalog</span></span>
```
PS C:\>New-AzureRmDataLakeAnalyticsCatalogSecret -Account "ContosoAdlAccount" -DatabaseName "databaseName" -Secret (Get-Credential) -Host "https://example.contoso.com" -Port 8080
```

<span data-ttu-id="beaa3-111">Bu komut belirtilen hesap, veritabanı, kimlik bilgisi ve ana bilgisayara karşılık gelen parolayı alır.</span><span class="sxs-lookup"><span data-stu-id="beaa3-111">This command gets the secret corresponding to the specified account, database, credential, and host.</span></span>

## <span data-ttu-id="beaa3-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="beaa3-112">PARAMETERS</span></span>

### <span data-ttu-id="beaa3-113">-Hesap</span><span class="sxs-lookup"><span data-stu-id="beaa3-113">-Account</span></span>
<span data-ttu-id="beaa3-114">Data Lake Analytics hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="beaa3-114">Specifies the name of the Data Lake Analytics account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="beaa3-115">-DatabaseHost</span><span class="sxs-lookup"><span data-stu-id="beaa3-115">-DatabaseHost</span></span>
<span data-ttu-id="beaa3-116">Parolanın ' mydatabase.contoso.com ' biçiminde ilişkilendirildiği veritabanının ana bilgisayar adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="beaa3-116">Specifies the host name for the database the secret is associated with in the format 'mydatabase.contoso.com'.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByFullURI
Aliases: Host

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="beaa3-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="beaa3-117">-DatabaseName</span></span>
<span data-ttu-id="beaa3-118">Parolayı içeren veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="beaa3-118">Specifies the name of the database that holds the secret.</span></span>

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

### <span data-ttu-id="beaa3-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="beaa3-119">-DefaultProfile</span></span>
<span data-ttu-id="beaa3-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="beaa3-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="beaa3-121">-Bağlantı noktası</span><span class="sxs-lookup"><span data-stu-id="beaa3-121">-Port</span></span>
<span data-ttu-id="beaa3-122">Parolanın bağlantı noktası numarasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="beaa3-122">Specifies the port number of the secret.</span></span>

```yaml
Type: System.Int32
Parameter Sets: CreateByFullURI
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="beaa3-123">-Parola</span><span class="sxs-lookup"><span data-stu-id="beaa3-123">-Secret</span></span>
<span data-ttu-id="beaa3-124">Parolanın adını ve parolasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="beaa3-124">Specifies the name and password of the secret.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="beaa3-125">-URI</span><span class="sxs-lookup"><span data-stu-id="beaa3-125">-Uri</span></span>
<span data-ttu-id="beaa3-126">Gizli kod kaynağının Tekdüzen Kaynak tanımlayıcısını (URI) belirtir.</span><span class="sxs-lookup"><span data-stu-id="beaa3-126">Specifies the Uniform Resource Identifier (URI) of the secret.</span></span>

```yaml
Type: System.Uri
Parameter Sets: CreateByHostNameAndPort
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="beaa3-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="beaa3-127">CommonParameters</span></span>
<span data-ttu-id="beaa3-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="beaa3-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="beaa3-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="beaa3-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="beaa3-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="beaa3-130">INPUTS</span></span>

### <span data-ttu-id="beaa3-131">System. String</span><span class="sxs-lookup"><span data-stu-id="beaa3-131">System.String</span></span>

### <span data-ttu-id="beaa3-132">System. Management. Automation. PSCredential</span><span class="sxs-lookup"><span data-stu-id="beaa3-132">System.Management.Automation.PSCredential</span></span>

### <span data-ttu-id="beaa3-133">System. Uri</span><span class="sxs-lookup"><span data-stu-id="beaa3-133">System.Uri</span></span>

### <span data-ttu-id="beaa3-134">System. Int32</span><span class="sxs-lookup"><span data-stu-id="beaa3-134">System.Int32</span></span>

## <span data-ttu-id="beaa3-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="beaa3-135">OUTPUTS</span></span>

### <span data-ttu-id="beaa3-136">Microsoft. Azure. Management. DataLake. Analytics. modeller. Usensecret</span><span class="sxs-lookup"><span data-stu-id="beaa3-136">Microsoft.Azure.Management.DataLake.Analytics.Models.USqlSecret</span></span>

## <span data-ttu-id="beaa3-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="beaa3-137">NOTES</span></span>

## <span data-ttu-id="beaa3-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="beaa3-138">RELATED LINKS</span></span>

[<span data-ttu-id="beaa3-139">Remove-Azurermdatalakeanalyzer Tic, Alogsecret</span><span class="sxs-lookup"><span data-stu-id="beaa3-139">Remove-AzureRmDataLakeAnalyticsCatalogSecret</span></span>](./Remove-AzureRmDataLakeAnalyticsCatalogSecret.md)

[<span data-ttu-id="beaa3-140">Set-Azurermdatalakeanalyzer Tic, Alogsecret</span><span class="sxs-lookup"><span data-stu-id="beaa3-140">Set-AzureRmDataLakeAnalyticsCatalogSecret</span></span>](./Set-AzureRmDataLakeAnalyticsCatalogSecret.md)

