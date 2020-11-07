---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 75E4E0FB-35A8-47DA-B606-45E073D04625
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/set-azdatalakeanalyticscatalogcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsCatalogCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsCatalogCredential.md
ms.openlocfilehash: 534608e2270cd2a3254096dc5b3def7310b7dc4d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916952"
---
# <span data-ttu-id="4ceea-101">Set-AzDataLakeAnalyticsCatalogCredential</span><span class="sxs-lookup"><span data-stu-id="4ceea-101">Set-AzDataLakeAnalyticsCatalogCredential</span></span>

## <span data-ttu-id="4ceea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4ceea-102">SYNOPSIS</span></span>
<span data-ttu-id="4ceea-103">Azure Data Lake Analytics Katalog kimlik bilgileri parolasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="4ceea-103">Modifies an Azure Data Lake Analytics catalog credential password.</span></span>

## <span data-ttu-id="4ceea-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4ceea-104">SYNTAX</span></span>

### <span data-ttu-id="4ceea-105">SetByHostNameAndPort (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="4ceea-105">SetByHostNameAndPort (Default)</span></span>
```
Set-AzDataLakeAnalyticsCatalogCredential [-Account] <String> [-DatabaseName] <String>
 [-CredentialName] <String> [-Credential] <PSCredential> [-NewPassword] <PSCredential> [-Uri] <Uri>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4ceea-106">SetByFullURI</span><span class="sxs-lookup"><span data-stu-id="4ceea-106">SetByFullURI</span></span>
```
Set-AzDataLakeAnalyticsCatalogCredential [-Account] <String> [-DatabaseName] <String>
 [-CredentialName] <String> [-Credential] <PSCredential> [-NewPassword] <PSCredential> [-DatabaseHost] <String>
 [-Port] <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4ceea-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="4ceea-107">DESCRIPTION</span></span>
<span data-ttu-id="4ceea-108">Set-AzDataLakeAnalyticsCatalogCredential cmdlet 'i Azure Data Lake Analytics kataloğu ile ilişkilendirilmiş bir kimlik bilgisi parolasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="4ceea-108">The Set-AzDataLakeAnalyticsCatalogCredential cmdlet modifies a credential password associated with an Azure Data Lake Analytics catalog.</span></span>

## <span data-ttu-id="4ceea-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4ceea-109">EXAMPLES</span></span>

### <span data-ttu-id="4ceea-110">Örnek 1: bir hesabın kimlik bilgilerinin parolasını değiştirme</span><span class="sxs-lookup"><span data-stu-id="4ceea-110">Example 1: Modify a credential's password associated with an account</span></span>
```
PS C:\> Set-AzDataLakeAnalyticsCatalogCredential -AccountName "ContosoAdlAccount" `
                  -DatabaseName "databaseName" `
                  -CredentialName "credName" `
                  -Credential (Get-Credential) `
                  -NewPassword (Get-Credential) `
                  -Host "example.contoso.com" -Port 8080
```

<span data-ttu-id="4ceea-111">Bu komut, kimlik bilgileri parolasını NewPassword 'de belirtilen parolayla ayarlar.</span><span class="sxs-lookup"><span data-stu-id="4ceea-111">This command sets the credential password to the password specified in NewPassword.</span></span>

## <span data-ttu-id="4ceea-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4ceea-112">PARAMETERS</span></span>

### <span data-ttu-id="4ceea-113">-Hesap</span><span class="sxs-lookup"><span data-stu-id="4ceea-113">-Account</span></span>
<span data-ttu-id="4ceea-114">Data Lake Analytics hesap adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4ceea-114">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="4ceea-115">-Credential</span><span class="sxs-lookup"><span data-stu-id="4ceea-115">-Credential</span></span>
<span data-ttu-id="4ceea-116">Değiştirilecek kimlik bilgisinin adını ve geçerli parolasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4ceea-116">Specifies the name and current password of the credential to modify.</span></span>

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

### <span data-ttu-id="4ceea-117">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="4ceea-117">-CredentialName</span></span>
<span data-ttu-id="4ceea-118">Değiştirilecek kimlik bilgisinin adını belirtir</span><span class="sxs-lookup"><span data-stu-id="4ceea-118">Specifies the name of the credential to modify</span></span>

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

### <span data-ttu-id="4ceea-119">-DatabaseHost</span><span class="sxs-lookup"><span data-stu-id="4ceea-119">-DatabaseHost</span></span>
<span data-ttu-id="4ceea-120">Kimlik bilgilerinin mydatabase.contoso.com biçiminde bağlanabileceği dış veri kaynağının ana bilgisayar adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4ceea-120">Specifies the host name of the external data source the credential can connect to in the format mydatabase.contoso.com.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByFullURI
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ceea-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="4ceea-121">-DatabaseName</span></span>
<span data-ttu-id="4ceea-122">Kimlik bilgilerini tutan Data Lake Analytics hesabındaki veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4ceea-122">Specifies the name of the database in the Data Lake Analytics account holding the credential.</span></span>

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

### <span data-ttu-id="4ceea-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ceea-123">-DefaultProfile</span></span>
<span data-ttu-id="4ceea-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="4ceea-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4ceea-125">-YeniParola</span><span class="sxs-lookup"><span data-stu-id="4ceea-125">-NewPassword</span></span>
<span data-ttu-id="4ceea-126">Kimlik bilgisinin yeni parolasını belirtir</span><span class="sxs-lookup"><span data-stu-id="4ceea-126">Specifies the new password for the credential</span></span>

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

### <span data-ttu-id="4ceea-127">-Bağlantı noktası</span><span class="sxs-lookup"><span data-stu-id="4ceea-127">-Port</span></span>
<span data-ttu-id="4ceea-128">Bu kimlik bilgisini kullanarak belirtilen DatabaseHost 'a bağlanmak için kullanılan bağlantı noktası numarasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4ceea-128">Specifies the port number used to connect to the specified DatabaseHost using this credential.</span></span>

```yaml
Type: System.Int32
Parameter Sets: SetByFullURI
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ceea-129">-URI</span><span class="sxs-lookup"><span data-stu-id="4ceea-129">-Uri</span></span>
<span data-ttu-id="4ceea-130">Bu kimlik bilgisinin bağlanabileceği dış veri kaynağının tam Tekdüzen Kaynak tanımlayıcısını (URI) belirtir.</span><span class="sxs-lookup"><span data-stu-id="4ceea-130">Specifies the full Uniform Resource Identifier (URI) of the external data source this credential can connect to.</span></span>

```yaml
Type: System.Uri
Parameter Sets: SetByHostNameAndPort
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ceea-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="4ceea-131">-Confirm</span></span>
<span data-ttu-id="4ceea-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4ceea-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ceea-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ceea-133">-WhatIf</span></span>
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

### <span data-ttu-id="4ceea-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ceea-134">CommonParameters</span></span>
<span data-ttu-id="4ceea-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4ceea-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ceea-136">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ceea-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ceea-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4ceea-137">INPUTS</span></span>

### <span data-ttu-id="4ceea-138">System. String</span><span class="sxs-lookup"><span data-stu-id="4ceea-138">System.String</span></span>

### <span data-ttu-id="4ceea-139">System. Management. Automation. PSCredential</span><span class="sxs-lookup"><span data-stu-id="4ceea-139">System.Management.Automation.PSCredential</span></span>

### <span data-ttu-id="4ceea-140">System. Uri</span><span class="sxs-lookup"><span data-stu-id="4ceea-140">System.Uri</span></span>

### <span data-ttu-id="4ceea-141">System. Int32</span><span class="sxs-lookup"><span data-stu-id="4ceea-141">System.Int32</span></span>

## <span data-ttu-id="4ceea-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4ceea-142">OUTPUTS</span></span>

### <span data-ttu-id="4ceea-143">Microsoft. Azure. Management. DataLake. Analytics. modeller. Ustocredential</span><span class="sxs-lookup"><span data-stu-id="4ceea-143">Microsoft.Azure.Management.DataLake.Analytics.Models.USqlCredential</span></span>

## <span data-ttu-id="4ceea-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4ceea-144">NOTES</span></span>

## <span data-ttu-id="4ceea-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4ceea-145">RELATED LINKS</span></span>
