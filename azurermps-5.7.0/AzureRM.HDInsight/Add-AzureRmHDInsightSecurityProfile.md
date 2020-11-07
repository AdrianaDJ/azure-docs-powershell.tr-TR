---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: FB37494B-4035-45B7-88AB-DF33CEEF0D0A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/add-azurermhdinsightsecurityprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Add-AzureRmHDInsightSecurityProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Add-AzureRmHDInsightSecurityProfile.md
ms.openlocfilehash: 41571439400810214bee7f0f3f646e6444998982
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762529"
---
# <span data-ttu-id="0d920-101">Add-AzureRmHDInsightSecurityProfile</span><span class="sxs-lookup"><span data-stu-id="0d920-101">Add-AzureRmHDInsightSecurityProfile</span></span>

## <span data-ttu-id="0d920-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0d920-102">SYNOPSIS</span></span>
<span data-ttu-id="0d920-103">Küme yapılandırma nesnesine bir güvenlik profilimi ekler.</span><span class="sxs-lookup"><span data-stu-id="0d920-103">Adds a security profileto a cluster configuration object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0d920-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0d920-104">SYNTAX</span></span>

```
Add-AzureRmHDInsightSecurityProfile [-Config] <AzureHDInsightConfig> -Domain <String>
 -DomainUserCredential <PSCredential> -OrganizationalUnitDN <String> -LdapsUrls <String[]>
 [-ClusterUsersGroupDNs <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0d920-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="0d920-105">DESCRIPTION</span></span>
<span data-ttu-id="0d920-106">Güvenlik profili, kerberizing tarafından güvenli bir küme oluşturmak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="0d920-106">Security profile is used to create a secure cluster by kerberizing it.</span></span>
<span data-ttu-id="0d920-107">Güvenlik profili, kümeyi Active Directory etki alanına katma ile ilgili yapılandırmayı içerir.</span><span class="sxs-lookup"><span data-stu-id="0d920-107">Security profile contains configuration related joining the cluster to Active Directory Domain.</span></span>

## <span data-ttu-id="0d920-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0d920-108">EXAMPLES</span></span>

### <span data-ttu-id="0d920-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="0d920-109">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="0d920-110">{{Buraya örnek açıklama ekleyin}}</span><span class="sxs-lookup"><span data-stu-id="0d920-110">{{ Add example description here }}</span></span>

## <span data-ttu-id="0d920-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0d920-111">PARAMETERS</span></span>

### <span data-ttu-id="0d920-112">-ClusterUsersGroupDNs</span><span class="sxs-lookup"><span data-stu-id="0d920-112">-ClusterUsersGroupDNs</span></span>
<span data-ttu-id="0d920-113">Sağlanan Active Directory gruplarının, bu ve Ranger 'ta kullanılabilir olacak ayırt edici adları</span><span class="sxs-lookup"><span data-stu-id="0d920-113">Distinguished names of the Active Directory groups that will be available in Ambari and Ranger</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d920-114">-Config</span><span class="sxs-lookup"><span data-stu-id="0d920-114">-Config</span></span>
<span data-ttu-id="0d920-115">Bu cmdlet 'in değiştirdiği HDInsight küme yapılandırması nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="0d920-115">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="0d920-116">Bu nesne New-AzureRmHDInsightClusterConfig cmdlet tarafından oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="0d920-116">This object is created by the New-AzureRmHDInsightClusterConfig cmdlet.</span></span>

```yaml
Type: AzureHDInsightConfig
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0d920-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d920-117">-DefaultProfile</span></span>
<span data-ttu-id="0d920-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="0d920-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0d920-119">-Etki alanı</span><span class="sxs-lookup"><span data-stu-id="0d920-119">-Domain</span></span>
<span data-ttu-id="0d920-120">Küme için Active Directory etki alanı</span><span class="sxs-lookup"><span data-stu-id="0d920-120">Active Directory domain for the cluster</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d920-121">-DomainUserCredential</span><span class="sxs-lookup"><span data-stu-id="0d920-121">-DomainUserCredential</span></span>
<span data-ttu-id="0d920-122">Kümeyi oluşturmak için yeterli izinlere sahip bir etki alanı kullanıcı hesabı kimlik bilgisi.</span><span class="sxs-lookup"><span data-stu-id="0d920-122">A domain user account credential with sufficient permissions for creating the cluster.</span></span>
<span data-ttu-id="0d920-123">Kullanıcı adı biçimde olmalıdır user@domain</span><span class="sxs-lookup"><span data-stu-id="0d920-123">Username should be in user@domain format</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d920-124">-LdapsUrls</span><span class="sxs-lookup"><span data-stu-id="0d920-124">-LdapsUrls</span></span>
<span data-ttu-id="0d920-125">Active Directory için bir veya birden çok LDAPS sunucusunun URL 'leri</span><span class="sxs-lookup"><span data-stu-id="0d920-125">Urls of one or multiple LDAPS servers for the Active Directory</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d920-126">-OrganizationalUnitDN</span><span class="sxs-lookup"><span data-stu-id="0d920-126">-OrganizationalUnitDN</span></span>
<span data-ttu-id="0d920-127">Kullanıcı ve bilgisayar hesaplarının oluşturulacağı Active Directory 'deki kuruluş biriminin ayırt edici adı</span><span class="sxs-lookup"><span data-stu-id="0d920-127">Distinguished name of the organizational unit in the Active directory where user and computer accounts will be created</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d920-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="0d920-128">-Confirm</span></span>
<span data-ttu-id="0d920-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0d920-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0d920-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d920-130">-WhatIf</span></span>
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

### <span data-ttu-id="0d920-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d920-131">CommonParameters</span></span>
<span data-ttu-id="0d920-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0d920-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d920-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d920-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d920-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0d920-134">INPUTS</span></span>

### <span data-ttu-id="0d920-135">AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="0d920-135">AzureHDInsightConfig</span></span>
<span data-ttu-id="0d920-136">Parametre ' config ', ardışık düzenin ' AzureHDInsightConfig ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="0d920-136">Parameter 'Config' accepts value of type 'AzureHDInsightConfig' from the pipeline</span></span>

## <span data-ttu-id="0d920-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0d920-137">OUTPUTS</span></span>

### <span data-ttu-id="0d920-138">Microsoft. Azure. Commands. HDInsight. modeller. AzureHDInsightSecurityProfile</span><span class="sxs-lookup"><span data-stu-id="0d920-138">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightSecurityProfile</span></span>

## <span data-ttu-id="0d920-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0d920-139">NOTES</span></span>

## <span data-ttu-id="0d920-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0d920-140">RELATED LINKS</span></span>

