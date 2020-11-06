---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 75E4E0FB-35A8-47DA-B606-45E073D04625
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/set-azurermdatalakeanalyticscatalogcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Set-AzureRmDataLakeAnalyticsCatalogCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Set-AzureRmDataLakeAnalyticsCatalogCredential.md
ms.openlocfilehash: 7c60e6cfca0cc045d016dd763f0b64b0ad3c6550
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589822"
---
# <span data-ttu-id="6d800-101">Set-AzureRmDataLakeAnalyticsCatalogCredential</span><span class="sxs-lookup"><span data-stu-id="6d800-101">Set-AzureRmDataLakeAnalyticsCatalogCredential</span></span>

## <span data-ttu-id="6d800-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6d800-102">SYNOPSIS</span></span>
<span data-ttu-id="6d800-103">Azure Data Lake Analytics Katalog kimlik bilgileri parolasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="6d800-103">Modifies an Azure Data Lake Analytics catalog credential password.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6d800-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6d800-104">SYNTAX</span></span>

### <span data-ttu-id="6d800-105">SetByHostNameAndPort (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="6d800-105">SetByHostNameAndPort (Default)</span></span>
```
Set-AzureRmDataLakeAnalyticsCatalogCredential [-Account] <String> [-DatabaseName] <String>
 [-CredentialName] <String> [-Credential] <PSCredential> [-NewPassword] <PSCredential> [-Uri] <Uri>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6d800-106">SetByFullURI</span><span class="sxs-lookup"><span data-stu-id="6d800-106">SetByFullURI</span></span>
```
Set-AzureRmDataLakeAnalyticsCatalogCredential [-Account] <String> [-DatabaseName] <String>
 [-CredentialName] <String> [-Credential] <PSCredential> [-NewPassword] <PSCredential> [-DatabaseHost] <String>
 [-Port] <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6d800-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="6d800-107">DESCRIPTION</span></span>
<span data-ttu-id="6d800-108">Set-AzureRmDataLakeAnalyticsCatalogCredential cmdlet 'i Azure Data Lake Analytics kataloğu ile ilişkilendirilmiş bir kimlik bilgisi parolasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="6d800-108">The Set-AzureRmDataLakeAnalyticsCatalogCredential cmdlet modifies a credential password associated with an Azure Data Lake Analytics catalog.</span></span>

## <span data-ttu-id="6d800-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6d800-109">EXAMPLES</span></span>

### <span data-ttu-id="6d800-110">Örnek 1: bir hesabın kimlik bilgilerinin parolasını değiştirme</span><span class="sxs-lookup"><span data-stu-id="6d800-110">Example 1: Modify a credential's password associated with an account</span></span>
```
PS C:\> Set-AzureRmDataLakeAnalyticsCatalogCredential -AccountName "ContosoAdlAccount" `
                  -DatabaseName "databaseName" `
                  -CredentialName "credName" `
                  -Credential (Get-Credential) `
                  -NewPassword (Get-Credential) `
                  -Host "example.contoso.com" -Port 8080
```

<span data-ttu-id="6d800-111">Bu komut, kimlik bilgileri parolasını NewPassword 'de belirtilen parolayla ayarlar.</span><span class="sxs-lookup"><span data-stu-id="6d800-111">This command sets the credential password to the password specified in NewPassword.</span></span>

## <span data-ttu-id="6d800-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6d800-112">PARAMETERS</span></span>

### <span data-ttu-id="6d800-113">-Hesap</span><span class="sxs-lookup"><span data-stu-id="6d800-113">-Account</span></span>
<span data-ttu-id="6d800-114">Data Lake Analytics hesap adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6d800-114">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="6d800-115">-Credential</span><span class="sxs-lookup"><span data-stu-id="6d800-115">-Credential</span></span>
<span data-ttu-id="6d800-116">Değiştirilecek kimlik bilgisinin adını ve geçerli parolasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6d800-116">Specifies the name and current password of the credential to modify.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d800-117">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="6d800-117">-CredentialName</span></span>
<span data-ttu-id="6d800-118">Değiştirilecek kimlik bilgisinin adını belirtir</span><span class="sxs-lookup"><span data-stu-id="6d800-118">Specifies the name of the credential to modify</span></span>

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

### <span data-ttu-id="6d800-119">-DatabaseHost</span><span class="sxs-lookup"><span data-stu-id="6d800-119">-DatabaseHost</span></span>
<span data-ttu-id="6d800-120">Kimlik bilgilerinin mydatabase.contoso.com biçiminde bağlanabileceği dış veri kaynağının ana bilgisayar adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6d800-120">Specifies the host name of the external data source the credential can connect to in the format mydatabase.contoso.com.</span></span>

```yaml
Type: String
Parameter Sets: SetByFullURI
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d800-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="6d800-121">-DatabaseName</span></span>
<span data-ttu-id="6d800-122">Kimlik bilgilerini tutan Data Lake Analytics hesabındaki veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6d800-122">Specifies the name of the database in the Data Lake Analytics account holding the credential.</span></span>

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

### <span data-ttu-id="6d800-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d800-123">-DefaultProfile</span></span>
<span data-ttu-id="6d800-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="6d800-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6d800-125">-YeniParola</span><span class="sxs-lookup"><span data-stu-id="6d800-125">-NewPassword</span></span>
<span data-ttu-id="6d800-126">Kimlik bilgisinin yeni parolasını belirtir</span><span class="sxs-lookup"><span data-stu-id="6d800-126">Specifies the new password for the credential</span></span>

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

### <span data-ttu-id="6d800-127">-Bağlantı noktası</span><span class="sxs-lookup"><span data-stu-id="6d800-127">-Port</span></span>
<span data-ttu-id="6d800-128">Bu kimlik bilgisini kullanarak belirtilen DatabaseHost 'a bağlanmak için kullanılan bağlantı noktası numarasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6d800-128">Specifies the port number used to connect to the specified DatabaseHost using this credential.</span></span>

```yaml
Type: Int32
Parameter Sets: SetByFullURI
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d800-129">-URI</span><span class="sxs-lookup"><span data-stu-id="6d800-129">-Uri</span></span>
<span data-ttu-id="6d800-130">Bu kimlik bilgisinin bağlanabileceği dış veri kaynağının tam Tekdüzen Kaynak tanımlayıcısını (URI) belirtir.</span><span class="sxs-lookup"><span data-stu-id="6d800-130">Specifies the full Uniform Resource Identifier (URI) of the external data source this credential can connect to.</span></span>

```yaml
Type: Uri
Parameter Sets: SetByHostNameAndPort
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d800-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="6d800-131">-Confirm</span></span>
<span data-ttu-id="6d800-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6d800-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6d800-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d800-133">-WhatIf</span></span>
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

### <span data-ttu-id="6d800-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d800-134">CommonParameters</span></span>
<span data-ttu-id="6d800-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6d800-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d800-136">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d800-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d800-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6d800-137">INPUTS</span></span>

### <span data-ttu-id="6d800-138">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="6d800-138">None</span></span>
<span data-ttu-id="6d800-139">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="6d800-139">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6d800-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6d800-140">OUTPUTS</span></span>

### <span data-ttu-id="6d800-141">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="6d800-141">None</span></span>

## <span data-ttu-id="6d800-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6d800-142">NOTES</span></span>

## <span data-ttu-id="6d800-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6d800-143">RELATED LINKS</span></span>

