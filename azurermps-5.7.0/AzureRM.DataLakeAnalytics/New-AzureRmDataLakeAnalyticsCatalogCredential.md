---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: BB6AF5A9-49BD-4A76-9F3F-44B62D2AB842
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/new-azurermdatalakeanalyticscatalogcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/New-AzureRmDataLakeAnalyticsCatalogCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/New-AzureRmDataLakeAnalyticsCatalogCredential.md
ms.openlocfilehash: 2dd97b310de764638fab029c60407c578287e9a9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588950"
---
# <span data-ttu-id="c848e-101">New-AzureRmDataLakeAnalyticsCatalogCredential</span><span class="sxs-lookup"><span data-stu-id="c848e-101">New-AzureRmDataLakeAnalyticsCatalogCredential</span></span>

## <span data-ttu-id="c848e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c848e-102">SYNOPSIS</span></span>
<span data-ttu-id="c848e-103">Yeni bir Azure Data Lake Analytics kataloğu kimlik bilgisi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c848e-103">Creates a new Azure Data Lake Analytics catalog credential.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c848e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c848e-104">SYNTAX</span></span>

### <span data-ttu-id="c848e-105">CreateByHostNameAndPort (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="c848e-105">CreateByHostNameAndPort (Default)</span></span>
```
New-AzureRmDataLakeAnalyticsCatalogCredential [-Account] <String> [-DatabaseName] <String>
 [-CredentialName] <String> [-Credential] <PSCredential> [-Uri] <Uri>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c848e-106">CreateByFullURI</span><span class="sxs-lookup"><span data-stu-id="c848e-106">CreateByFullURI</span></span>
```
New-AzureRmDataLakeAnalyticsCatalogCredential [-Account] <String> [-DatabaseName] <String>
 [-CredentialName] <String> [-Credential] <PSCredential> [-DatabaseHost] <String> [-Port] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c848e-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="c848e-107">DESCRIPTION</span></span>
<span data-ttu-id="c848e-108">New-AzureRmDataLakeAnalyticsCatalogCredential cmdlet, dış veri kaynaklarına bağlanmak için bir Azure Data Lake Analytics kataloğunda kullanılacak yeni bir kimlik bilgisi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c848e-108">The New-AzureRmDataLakeAnalyticsCatalogCredential cmdlet creates a new credential to use in an Azure Data Lake Analytics catalog for connecting to external data sources.</span></span>

## <span data-ttu-id="c848e-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c848e-109">EXAMPLES</span></span>

### <span data-ttu-id="c848e-110">Örnek 1: Ana bilgisayar ve bağlantı noktası belirten bir katalog kimlik bilgisi oluşturma</span><span class="sxs-lookup"><span data-stu-id="c848e-110">Example 1: Create a credential for a catalog specifying host and port</span></span>
```
PS C:\> New-AzureRmDataLakeAnalyticsCatalogCredential -AccountName "ContosoAdlAccount" `
                  -DatabaseName "databaseName" `
                  -CredentialName "exampleDbCred" `
                  -Credential (Get-Credential) `
                  -DatabaseHost "example.contoso.com" -Port 8080
```

<span data-ttu-id="c848e-111">Bu komut, https protokolünü kullanan belirtilen hesap, veritabanı, ana bilgisayar ve bağlantı noktası için belirtilen kimlik bilgilerini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c848e-111">This command creates the specified credential for the specified account, database, host and port using https protocol.</span></span>

### <span data-ttu-id="c848e-112">Örnek 2: tam URI 'yi belirten bir katalog kimlik bilgisi oluşturma</span><span class="sxs-lookup"><span data-stu-id="c848e-112">Example 2: Create a credential for a catalog specifying full URI</span></span>
```
PS C:\> New-AzureRmDataLakeAnalyticsCatalogCredential -AccountName "ContosoAdlAccount" `
                  -DatabaseName "databaseName" `
                  -CredentialName "exampleDbCred" `
                  -Credential (Get-Credential) `
                  -Uri "http://httpExample.contoso.com:8080"
```

<span data-ttu-id="c848e-113">Bu komut belirtilen hesap, veritabanı ve dış veri kaynağı URI 'SI için belirtilen kimlik bilgilerini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c848e-113">This command creates the specified credential for the specified account, database and external data source URI.</span></span>

## <span data-ttu-id="c848e-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c848e-114">PARAMETERS</span></span>

### <span data-ttu-id="c848e-115">-Hesap</span><span class="sxs-lookup"><span data-stu-id="c848e-115">-Account</span></span>
<span data-ttu-id="c848e-116">Data Lake Analytics hesap adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c848e-116">Specifies the Data Lake Analytics account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c848e-117">-Credential</span><span class="sxs-lookup"><span data-stu-id="c848e-117">-Credential</span></span>
<span data-ttu-id="c848e-118">Kimlik bilgisinin Kullanıcı adını ve karşılık gelen parolasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c848e-118">Specifies the user name and corresponding password of the credential.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c848e-119">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="c848e-119">-CredentialName</span></span>
<span data-ttu-id="c848e-120">Kimlik bilgisinin adını ve parolasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c848e-120">Specifies the name and password of the credential.</span></span>

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

### <span data-ttu-id="c848e-121">-DatabaseHost</span><span class="sxs-lookup"><span data-stu-id="c848e-121">-DatabaseHost</span></span>
<span data-ttu-id="c848e-122">Kimlik bilgilerinin mydatabase.contoso.com biçiminde bağlanabileceği dış veri kaynağının ana bilgisayar adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c848e-122">Specifies the host name of the external data source the credential can connect to in the format mydatabase.contoso.com.</span></span>

```yaml
Type: String
Parameter Sets: CreateByFullURI
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c848e-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="c848e-123">-DatabaseName</span></span>
<span data-ttu-id="c848e-124">Veri Lake Analytics acoc, kimlik bilgisinin içinde saklanacağı veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c848e-124">Specifies the name of the database in the Data Lake Analytics acocunt that the credential will be stored in.</span></span>

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

### <span data-ttu-id="c848e-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c848e-125">-DefaultProfile</span></span>
<span data-ttu-id="c848e-126">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="c848e-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c848e-127">-Bağlantı noktası</span><span class="sxs-lookup"><span data-stu-id="c848e-127">-Port</span></span>
<span data-ttu-id="c848e-128">Bu kimlik bilgisini kullanarak belirtilen DatabaseHost 'a bağlanmak için kullanılan bağlantı noktası numarasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c848e-128">Specifies the port number used to connect to the specified DatabaseHost using this credential.</span></span>

```yaml
Type: Int32
Parameter Sets: CreateByFullURI
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c848e-129">-URI</span><span class="sxs-lookup"><span data-stu-id="c848e-129">-Uri</span></span>
<span data-ttu-id="c848e-130">Bu kimlik bilgisinin bağlanabileceği dış veri kaynağının tam Tekdüzen Kaynak tanımlayıcısını (URI) belirtir.</span><span class="sxs-lookup"><span data-stu-id="c848e-130">Specifies the full Uniform Resource Identifier (URI) of the external data source this credential can connect to.</span></span>

```yaml
Type: Uri
Parameter Sets: CreateByHostNameAndPort
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c848e-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="c848e-131">-Confirm</span></span>
<span data-ttu-id="c848e-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c848e-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c848e-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c848e-133">-WhatIf</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c848e-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c848e-134">CommonParameters</span></span>
<span data-ttu-id="c848e-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c848e-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c848e-136">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c848e-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c848e-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c848e-137">INPUTS</span></span>

### <span data-ttu-id="c848e-138">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="c848e-138">None</span></span>
<span data-ttu-id="c848e-139">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="c848e-139">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c848e-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c848e-140">OUTPUTS</span></span>

### <span data-ttu-id="c848e-141">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="c848e-141">None</span></span>

## <span data-ttu-id="c848e-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c848e-142">NOTES</span></span>

## <span data-ttu-id="c848e-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c848e-143">RELATED LINKS</span></span>

