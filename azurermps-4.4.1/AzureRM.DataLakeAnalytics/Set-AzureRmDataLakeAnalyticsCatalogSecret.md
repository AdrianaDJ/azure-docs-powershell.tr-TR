---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: CAB32C72-5C16-467E-BC57-749EC49916BB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Set-AzureRmDataLakeAnalyticsCatalogSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Set-AzureRmDataLakeAnalyticsCatalogSecret.md
ms.openlocfilehash: e807d1fd1c630554bbaefe0cae1dd225b5f1a184
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763770"
---
# <span data-ttu-id="4e772-101">Set-AzureRmDataLakeAnalyticsCatalogSecret</span><span class="sxs-lookup"><span data-stu-id="4e772-101">Set-AzureRmDataLakeAnalyticsCatalogSecret</span></span>

## <span data-ttu-id="4e772-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4e772-102">SYNOPSIS</span></span>
<span data-ttu-id="4e772-103">Veri Lake Analytics Katalog gizliliğini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="4e772-103">Modifies a Data Lake Analytics catalog secret.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4e772-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4e772-104">SYNTAX</span></span>

### <span data-ttu-id="4e772-105">Tam URI 'yi belirtme</span><span class="sxs-lookup"><span data-stu-id="4e772-105">Specify full URI</span></span>
```
Set-AzureRmDataLakeAnalyticsCatalogSecret [-Account] <String> [-DatabaseName] <String> [-Secret] <PSCredential>
 [-DatabaseHost] <String> [-Port] <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4e772-106">Ana bilgisayar adı ve bağlantı noktası belirtme</span><span class="sxs-lookup"><span data-stu-id="4e772-106">Specify host name and port</span></span>
```
Set-AzureRmDataLakeAnalyticsCatalogSecret [-Account] <String> [-DatabaseName] <String> [-Secret] <PSCredential>
 [-Uri] <Uri> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4e772-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="4e772-107">DESCRIPTION</span></span>
<span data-ttu-id="4e772-108">**Set-Azurermdatalakeanalyzer Ticdağındağın**</span><span class="sxs-lookup"><span data-stu-id="4e772-108">The **Set-AzureRmDataLakeAnalyticsCatalogSecret** cmdlet modifies a secret associated with an Azure Data Lake Analytics catalog.</span></span>

## <span data-ttu-id="4e772-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4e772-109">EXAMPLES</span></span>

### <span data-ttu-id="4e772-110">Örnek 1: hesapla ilişkili gizli kod</span><span class="sxs-lookup"><span data-stu-id="4e772-110">Example 1: Modify the secret associated with an account</span></span>
```
PS C:\>Set-AzureRmDataLakeAnalyticsCatalogSecret -Account "ContosoAdlAccount" -DatabaseName "databaseName" -Secret (Get-Credential) -Host "https://example.contoso.com" -Port 8080
```

<span data-ttu-id="4e772-111">Bu komut, Data Lake Analytics kataloğu ile ilişkilendirilen gizliliği ayarlar.</span><span class="sxs-lookup"><span data-stu-id="4e772-111">This command sets the secret associated with a Data Lake Analytics catalog.</span></span>

## <span data-ttu-id="4e772-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4e772-112">PARAMETERS</span></span>

### <span data-ttu-id="4e772-113">-Hesap</span><span class="sxs-lookup"><span data-stu-id="4e772-113">-Account</span></span>
<span data-ttu-id="4e772-114">Data Lake Analytics hesap adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4e772-114">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="4e772-115">-DatabaseHost</span><span class="sxs-lookup"><span data-stu-id="4e772-115">-DatabaseHost</span></span>
<span data-ttu-id="4e772-116">Parolanın ' mydatabase.contoso.com ' biçiminde ilişkilendirildiği veritabanının ana bilgisayar adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4e772-116">Specifies the host name for the database the secret is associated with in the format 'mydatabase.contoso.com'.</span></span>

```yaml
Type: System.String
Parameter Sets: Specify full URI
Aliases: Host

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e772-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="4e772-117">-DatabaseName</span></span>
<span data-ttu-id="4e772-118">Parolayı içeren veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4e772-118">Specifies the name of the database holding the secret.</span></span>

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

### <span data-ttu-id="4e772-119">-Bağlantı noktası</span><span class="sxs-lookup"><span data-stu-id="4e772-119">-Port</span></span>
<span data-ttu-id="4e772-120">Parolanın bağlantı noktası numarasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4e772-120">Specifies the port number of the secret.</span></span>

```yaml
Type: System.Int32
Parameter Sets: Specify full URI
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e772-121">-Parola</span><span class="sxs-lookup"><span data-stu-id="4e772-121">-Secret</span></span>
<span data-ttu-id="4e772-122">Parolanın adını ve parolasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4e772-122">Specifies the name and password of the secret.</span></span>

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

### <span data-ttu-id="4e772-123">-URI</span><span class="sxs-lookup"><span data-stu-id="4e772-123">-Uri</span></span>
<span data-ttu-id="4e772-124">Gizli anahtar kaynağı tanımlayıcısını (URI) belirtir.</span><span class="sxs-lookup"><span data-stu-id="4e772-124">Specifies the Uniform Resource Identifier (URI) for the secret.</span></span>

```yaml
Type: System.Uri
Parameter Sets: Specify host name and port
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e772-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e772-125">-DefaultProfile</span></span>
<span data-ttu-id="4e772-126">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4e772-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4e772-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e772-127">CommonParameters</span></span>
<span data-ttu-id="4e772-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4e772-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e772-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e772-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e772-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4e772-130">INPUTS</span></span>

## <span data-ttu-id="4e772-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4e772-131">OUTPUTS</span></span>

### <span data-ttu-id="4e772-132">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="4e772-132">None</span></span>

## <span data-ttu-id="4e772-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4e772-133">NOTES</span></span>

## <span data-ttu-id="4e772-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4e772-134">RELATED LINKS</span></span>

[<span data-ttu-id="4e772-135">Yeni-Azurermdatalakeanalyzer Tic, Alogsecret</span><span class="sxs-lookup"><span data-stu-id="4e772-135">New-AzureRmDataLakeAnalyticsCatalogSecret</span></span>](./New-AzureRmDataLakeAnalyticsCatalogSecret.md)

[<span data-ttu-id="4e772-136">Remove-Azurermdatalakeanalyzer Tic, Alogsecret</span><span class="sxs-lookup"><span data-stu-id="4e772-136">Remove-AzureRmDataLakeAnalyticsCatalogSecret</span></span>](./Remove-AzureRmDataLakeAnalyticsCatalogSecret.md)


