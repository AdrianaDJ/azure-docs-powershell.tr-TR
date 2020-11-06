---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: FB37494B-4035-45B7-88AB-DF33CEEF0D0A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Add-AzureRmHDInsightSecurityProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Add-AzureRmHDInsightSecurityProfile.md
ms.openlocfilehash: 7ea9f9d9bb07cae6db62c51b9d496f7117eee700
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593562"
---
# <span data-ttu-id="48f4d-101">Add-AzureRmHDInsightSecurityProfile</span><span class="sxs-lookup"><span data-stu-id="48f4d-101">Add-AzureRmHDInsightSecurityProfile</span></span>

## <span data-ttu-id="48f4d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="48f4d-102">SYNOPSIS</span></span>
<span data-ttu-id="48f4d-103">Küme yapılandırma nesnesine bir güvenlik profilimi ekler.</span><span class="sxs-lookup"><span data-stu-id="48f4d-103">Adds a security profileto a cluster configuration object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="48f4d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="48f4d-104">SYNTAX</span></span>

```
Add-AzureRmHDInsightSecurityProfile [-Config] <AzureHDInsightConfig> -Domain <String>
 -DomainUserCredential <PSCredential> -OrganizationalUnitDN <String> -LdapsUrls <String[]>
 [-ClusterUsersGroupDNs <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="48f4d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="48f4d-105">DESCRIPTION</span></span>
<span data-ttu-id="48f4d-106">Güvenlik profili, kerberizing tarafından güvenli bir küme oluşturmak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="48f4d-106">Security profile is used to create a secure cluster by kerberizing it.</span></span>
<span data-ttu-id="48f4d-107">Güvenlik profili, kümeyi Active Directory etki alanına katma ile ilgili yapılandırmayı içerir.</span><span class="sxs-lookup"><span data-stu-id="48f4d-107">Security profile contains configuration related joining the cluster to Active Directory Domain.</span></span>

## <span data-ttu-id="48f4d-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="48f4d-108">EXAMPLES</span></span>

### <span data-ttu-id="48f4d-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="48f4d-109">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="48f4d-110">{{Buraya örnek açıklama ekleyin}}</span><span class="sxs-lookup"><span data-stu-id="48f4d-110">{{ Add example description here }}</span></span>

## <span data-ttu-id="48f4d-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="48f4d-111">PARAMETERS</span></span>

### <span data-ttu-id="48f4d-112">-ClusterUsersGroupDNs</span><span class="sxs-lookup"><span data-stu-id="48f4d-112">-ClusterUsersGroupDNs</span></span>
<span data-ttu-id="48f4d-113">Sağlanan Active Directory gruplarının, bu ve Ranger 'ta kullanılabilir olacak ayırt edici adları</span><span class="sxs-lookup"><span data-stu-id="48f4d-113">Distinguished names of the Active Directory groups that will be available in Ambari and Ranger</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48f4d-114">-Config</span><span class="sxs-lookup"><span data-stu-id="48f4d-114">-Config</span></span>
<span data-ttu-id="48f4d-115">Bu cmdlet 'in değiştirdiği HDInsight küme yapılandırması nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="48f4d-115">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="48f4d-116">Bu nesne New-AzureRmHDInsightClusterConfig cmdlet tarafından oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="48f4d-116">This object is created by the New-AzureRmHDInsightClusterConfig cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="48f4d-117">-Etki alanı</span><span class="sxs-lookup"><span data-stu-id="48f4d-117">-Domain</span></span>
<span data-ttu-id="48f4d-118">Küme için Active Directory etki alanı</span><span class="sxs-lookup"><span data-stu-id="48f4d-118">Active Directory domain for the cluster</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48f4d-119">-DomainUserCredential</span><span class="sxs-lookup"><span data-stu-id="48f4d-119">-DomainUserCredential</span></span>
<span data-ttu-id="48f4d-120">Kümeyi oluşturmak için yeterli izinlere sahip bir etki alanı kullanıcı hesabı kimlik bilgisi.</span><span class="sxs-lookup"><span data-stu-id="48f4d-120">A domain user account credential with sufficient permissions for creating the cluster.</span></span>
<span data-ttu-id="48f4d-121">Kullanıcı adı biçimde olmalıdır user@domain</span><span class="sxs-lookup"><span data-stu-id="48f4d-121">Username should be in user@domain format</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48f4d-122">-LdapsUrls</span><span class="sxs-lookup"><span data-stu-id="48f4d-122">-LdapsUrls</span></span>
<span data-ttu-id="48f4d-123">Active Directory için bir veya birden çok LDAPS sunucusunun URL 'leri</span><span class="sxs-lookup"><span data-stu-id="48f4d-123">Urls of one or multiple LDAPS servers for the Active Directory</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48f4d-124">-OrganizationalUnitDN</span><span class="sxs-lookup"><span data-stu-id="48f4d-124">-OrganizationalUnitDN</span></span>
<span data-ttu-id="48f4d-125">Kullanıcı ve bilgisayar hesaplarının oluşturulacağı Active Directory 'deki kuruluş biriminin ayırt edici adı</span><span class="sxs-lookup"><span data-stu-id="48f4d-125">Distinguished name of the organizational unit in the Active directory where user and computer accounts will be created</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48f4d-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="48f4d-126">-Confirm</span></span>
<span data-ttu-id="48f4d-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="48f4d-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="48f4d-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="48f4d-128">-WhatIf</span></span>
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

### <span data-ttu-id="48f4d-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48f4d-129">-DefaultProfile</span></span>
<span data-ttu-id="48f4d-130">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="48f4d-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="48f4d-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48f4d-131">CommonParameters</span></span>
<span data-ttu-id="48f4d-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="48f4d-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48f4d-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="48f4d-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48f4d-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="48f4d-134">INPUTS</span></span>

### <span data-ttu-id="48f4d-135">AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="48f4d-135">AzureHDInsightConfig</span></span>
<span data-ttu-id="48f4d-136">Parametre ' config ', ardışık düzenin ' AzureHDInsightConfig ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="48f4d-136">Parameter 'Config' accepts value of type 'AzureHDInsightConfig' from the pipeline</span></span>

## <span data-ttu-id="48f4d-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="48f4d-137">OUTPUTS</span></span>

### <span data-ttu-id="48f4d-138">Microsoft. Azure. Commands. HDInsight. modeller. AzureHDInsightSecurityProfile</span><span class="sxs-lookup"><span data-stu-id="48f4d-138">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightSecurityProfile</span></span>

## <span data-ttu-id="48f4d-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="48f4d-139">NOTES</span></span>

## <span data-ttu-id="48f4d-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="48f4d-140">RELATED LINKS</span></span>

