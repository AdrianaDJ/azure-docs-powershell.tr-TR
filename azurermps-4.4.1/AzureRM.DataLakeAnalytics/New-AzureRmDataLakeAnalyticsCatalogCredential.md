---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: BB6AF5A9-49BD-4A76-9F3F-44B62D2AB842
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/New-AzureRmDataLakeAnalyticsCatalogCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/New-AzureRmDataLakeAnalyticsCatalogCredential.md
ms.openlocfilehash: 1668ca10c8c3425bea7c4082033abb19f8de7306
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587959"
---
# <span data-ttu-id="0a019-101">New-AzureRmDataLakeAnalyticsCatalogCredential</span><span class="sxs-lookup"><span data-stu-id="0a019-101">New-AzureRmDataLakeAnalyticsCatalogCredential</span></span>

## <span data-ttu-id="0a019-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0a019-102">SYNOPSIS</span></span>
<span data-ttu-id="0a019-103">Yeni bir Azure Data Lake Analytics kataloğu kimlik bilgisi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0a019-103">Creates a new Azure Data Lake Analytics catalog credential.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0a019-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0a019-104">SYNTAX</span></span>

### <span data-ttu-id="0a019-105">Ana bilgisayar adını ve bağlantı noktasını belirtme (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="0a019-105">Specify host name and port (Default)</span></span>
```
New-AzureRmDataLakeAnalyticsCatalogCredential [-Account] <String> [-DatabaseName] <String>
 [-CredentialName] <String> [-Credential] <PSCredential> [-Uri] <Uri>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a019-106">Tam URI 'yi belirtme</span><span class="sxs-lookup"><span data-stu-id="0a019-106">Specify full URI</span></span>
```
New-AzureRmDataLakeAnalyticsCatalogCredential [-Account] <String> [-DatabaseName] <String>
 [-CredentialName] <String> [-Credential] <PSCredential> [-DatabaseHost] <String> [-Port] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0a019-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="0a019-107">DESCRIPTION</span></span>
<span data-ttu-id="0a019-108">New-AzureRmDataLakeAnalyticsCatalogCredential cmdlet, dış veri kaynaklarına bağlanmak için bir Azure Data Lake Analytics kataloğunda kullanılacak yeni bir kimlik bilgisi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0a019-108">The New-AzureRmDataLakeAnalyticsCatalogCredential cmdlet creates a new credential to use in an Azure Data Lake Analytics catalog for connecting to external data sources.</span></span>

## <span data-ttu-id="0a019-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0a019-109">EXAMPLES</span></span>

### <span data-ttu-id="0a019-110">Örnek 1: Ana bilgisayar ve bağlantı noktası belirten bir katalog kimlik bilgisi oluşturma</span><span class="sxs-lookup"><span data-stu-id="0a019-110">Example 1: Create a credential for a catalog specifying host and port</span></span>
```
PS C:\> New-AzureRmDataLakeAnalyticsCatalogCredential -AccountName "ContosoAdlAccount" `
                  -DatabaseName "databaseName" `
                  -CredentialName "exampleDbCred" `
                  -Credential (Get-Credential) `
                  -DatabaseHost "example.contoso.com" -Port 8080
```

<span data-ttu-id="0a019-111">Bu komut, https protokolünü kullanan belirtilen hesap, veritabanı, ana bilgisayar ve bağlantı noktası için belirtilen kimlik bilgilerini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0a019-111">This command creates the specified credential for the specified account, database, host and port using https protocol.</span></span>

### <span data-ttu-id="0a019-112">Örnek 2: tam URI 'yi belirten bir katalog kimlik bilgisi oluşturma</span><span class="sxs-lookup"><span data-stu-id="0a019-112">Example 2: Create a credential for a catalog specifying full URI</span></span>
```
PS C:\> New-AzureRmDataLakeAnalyticsCatalogCredential -AccountName "ContosoAdlAccount" `
                  -DatabaseName "databaseName" `
                  -CredentialName "exampleDbCred" `
                  -Credential (Get-Credential) `
                  -Uri "http://httpExample.contoso.com:8080"
```

<span data-ttu-id="0a019-113">Bu komut belirtilen hesap, veritabanı ve dış veri kaynağı URI 'SI için belirtilen kimlik bilgilerini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0a019-113">This command creates the specified credential for the specified account, database and external data source URI.</span></span>

## <span data-ttu-id="0a019-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0a019-114">PARAMETERS</span></span>

### <span data-ttu-id="0a019-115">-Hesap</span><span class="sxs-lookup"><span data-stu-id="0a019-115">-Account</span></span>
<span data-ttu-id="0a019-116">Data Lake Analytics hesap adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0a019-116">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="0a019-117">-Credential</span><span class="sxs-lookup"><span data-stu-id="0a019-117">-Credential</span></span>
<span data-ttu-id="0a019-118">Kimlik bilgisinin Kullanıcı adını ve karşılık gelen parolasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0a019-118">Specifies the user name and corresponding password of the credential.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a019-119">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="0a019-119">-CredentialName</span></span>
<span data-ttu-id="0a019-120">Kimlik bilgisinin adını ve parolasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0a019-120">Specifies the name and password of the credential.</span></span>

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

### <span data-ttu-id="0a019-121">-DatabaseHost</span><span class="sxs-lookup"><span data-stu-id="0a019-121">-DatabaseHost</span></span>
<span data-ttu-id="0a019-122">Kimlik bilgilerinin mydatabase.contoso.com biçiminde bağlanabileceği dış veri kaynağının ana bilgisayar adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0a019-122">Specifies the host name of the external data source the credential can connect to in the format mydatabase.contoso.com.</span></span>

```yaml
Type: System.String
Parameter Sets: Specify full URI
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a019-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="0a019-123">-DatabaseName</span></span>
<span data-ttu-id="0a019-124">Veri Lake Analytics acoc, kimlik bilgisinin içinde saklanacağı veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0a019-124">Specifies the name of the database in the Data Lake Analytics acocunt that the credential will be stored in.</span></span>

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

### <span data-ttu-id="0a019-125">-Bağlantı noktası</span><span class="sxs-lookup"><span data-stu-id="0a019-125">-Port</span></span>
<span data-ttu-id="0a019-126">Bu kimlik bilgisini kullanarak belirtilen DatabaseHost 'a bağlanmak için kullanılan bağlantı noktası numarasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0a019-126">Specifies the port number used to connect to the specified DatabaseHost using this credential.</span></span>

```yaml
Type: System.Int32
Parameter Sets: Specify full URI
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a019-127">-URI</span><span class="sxs-lookup"><span data-stu-id="0a019-127">-Uri</span></span>
<span data-ttu-id="0a019-128">Bu kimlik bilgisinin bağlanabileceği dış veri kaynağının tam Tekdüzen Kaynak tanımlayıcısını (URI) belirtir.</span><span class="sxs-lookup"><span data-stu-id="0a019-128">Specifies the full Uniform Resource Identifier (URI) of the external data source this credential can connect to.</span></span>

```yaml
Type: System.Uri
Parameter Sets: Specify host name and port
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a019-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="0a019-129">-Confirm</span></span>
<span data-ttu-id="0a019-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0a019-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a019-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0a019-131">-WhatIf</span></span>
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a019-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a019-132">-DefaultProfile</span></span>
<span data-ttu-id="0a019-133">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0a019-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0a019-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a019-134">CommonParameters</span></span>
<span data-ttu-id="0a019-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0a019-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a019-136">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a019-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a019-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0a019-137">INPUTS</span></span>

## <span data-ttu-id="0a019-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0a019-138">OUTPUTS</span></span>

### <span data-ttu-id="0a019-139">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="0a019-139">None</span></span>

## <span data-ttu-id="0a019-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0a019-140">NOTES</span></span>

## <span data-ttu-id="0a019-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0a019-141">RELATED LINKS</span></span>

