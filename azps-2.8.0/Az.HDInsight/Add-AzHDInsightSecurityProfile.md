---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: FB37494B-4035-45B7-88AB-DF33CEEF0D0A
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/add-azhdinsightsecurityprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightSecurityProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightSecurityProfile.md
ms.openlocfilehash: c0e54e92336b7b084448a980f632c886c24dc07c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93751861"
---
# <span data-ttu-id="a9732-101">Add-AzHDInsightSecurityProfile</span><span class="sxs-lookup"><span data-stu-id="a9732-101">Add-AzHDInsightSecurityProfile</span></span>

## <span data-ttu-id="a9732-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a9732-102">SYNOPSIS</span></span>
<span data-ttu-id="a9732-103">Küme yapılandırma nesnesine güvenlik profili ekler.</span><span class="sxs-lookup"><span data-stu-id="a9732-103">Adds a security profile to a cluster configuration object.</span></span>

## <span data-ttu-id="a9732-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a9732-104">SYNTAX</span></span>

```
Add-AzHDInsightSecurityProfile [-Config] <AzureHDInsightConfig> -Domain <String>
 -DomainUserCredential <PSCredential> -OrganizationalUnitDN <String> -LdapsUrls <String[]>
 [-ClusterUsersGroupDNs <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a9732-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a9732-105">DESCRIPTION</span></span>
<span data-ttu-id="a9732-106">Güvenlik profili, kerberizing tarafından güvenli bir küme oluşturmak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="a9732-106">Security profile is used to create a secure cluster by kerberizing it.</span></span>
<span data-ttu-id="a9732-107">Güvenlik profili, kümeyi Active Directory etki alanına katma ile ilgili yapılandırmayı içerir.</span><span class="sxs-lookup"><span data-stu-id="a9732-107">Security profile contains configuration related joining the cluster to Active Directory Domain.</span></span>

## <span data-ttu-id="a9732-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a9732-108">EXAMPLES</span></span>

### <span data-ttu-id="a9732-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="a9732-109">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="a9732-110">{{Buraya örnek açıklama ekleyin}}</span><span class="sxs-lookup"><span data-stu-id="a9732-110">{{ Add example description here }}</span></span>

## <span data-ttu-id="a9732-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a9732-111">PARAMETERS</span></span>

### <span data-ttu-id="a9732-112">-ClusterUsersGroupDNs</span><span class="sxs-lookup"><span data-stu-id="a9732-112">-ClusterUsersGroupDNs</span></span>
<span data-ttu-id="a9732-113">Sağlanan Active Directory gruplarının, bu ve Ranger 'ta kullanılabilir olacak ayırt edici adları</span><span class="sxs-lookup"><span data-stu-id="a9732-113">Distinguished names of the Active Directory groups that will be available in Ambari and Ranger</span></span>

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

### <span data-ttu-id="a9732-114">-Config</span><span class="sxs-lookup"><span data-stu-id="a9732-114">-Config</span></span>
<span data-ttu-id="a9732-115">Bu cmdlet 'in değiştirdiği HDInsight küme yapılandırması nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a9732-115">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="a9732-116">Bu nesne New-AzHDInsightClusterConfig cmdlet tarafından oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="a9732-116">This object is created by the New-AzHDInsightClusterConfig cmdlet.</span></span>

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

### <span data-ttu-id="a9732-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9732-117">-DefaultProfile</span></span>
<span data-ttu-id="a9732-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="a9732-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a9732-119">-Etki alanı</span><span class="sxs-lookup"><span data-stu-id="a9732-119">-Domain</span></span>
<span data-ttu-id="a9732-120">Küme için Active Directory etki alanı</span><span class="sxs-lookup"><span data-stu-id="a9732-120">Active Directory domain for the cluster</span></span>

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

### <span data-ttu-id="a9732-121">-DomainUserCredential</span><span class="sxs-lookup"><span data-stu-id="a9732-121">-DomainUserCredential</span></span>
<span data-ttu-id="a9732-122">Kümeyi oluşturmak için yeterli izinlere sahip bir etki alanı kullanıcı hesabı kimlik bilgisi.</span><span class="sxs-lookup"><span data-stu-id="a9732-122">A domain user account credential with sufficient permissions for creating the cluster.</span></span>
<span data-ttu-id="a9732-123">Kullanıcı adı biçimde olmalıdır user@domain</span><span class="sxs-lookup"><span data-stu-id="a9732-123">Username should be in user@domain format</span></span>

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

### <span data-ttu-id="a9732-124">-LdapsUrls</span><span class="sxs-lookup"><span data-stu-id="a9732-124">-LdapsUrls</span></span>
<span data-ttu-id="a9732-125">Active Directory için bir veya birden çok LDAPS sunucusunun URL 'leri</span><span class="sxs-lookup"><span data-stu-id="a9732-125">Urls of one or multiple LDAPS servers for the Active Directory</span></span>

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

### <span data-ttu-id="a9732-126">-OrganizationalUnitDN</span><span class="sxs-lookup"><span data-stu-id="a9732-126">-OrganizationalUnitDN</span></span>
<span data-ttu-id="a9732-127">Kullanıcı ve bilgisayar hesaplarının oluşturulacağı Active Directory 'deki kuruluş biriminin ayırt edici adı</span><span class="sxs-lookup"><span data-stu-id="a9732-127">Distinguished name of the organizational unit in the Active directory where user and computer accounts will be created</span></span>

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

### <span data-ttu-id="a9732-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="a9732-128">-Confirm</span></span>
<span data-ttu-id="a9732-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a9732-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a9732-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9732-130">-WhatIf</span></span>
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

### <span data-ttu-id="a9732-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9732-131">CommonParameters</span></span>
<span data-ttu-id="a9732-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a9732-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9732-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9732-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9732-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a9732-134">INPUTS</span></span>

### <span data-ttu-id="a9732-135">Microsoft. Azure. Commands. HDInsight. modeller. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="a9732-135">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="a9732-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a9732-136">OUTPUTS</span></span>

### <span data-ttu-id="a9732-137">Microsoft. Azure. Commands. HDInsight. modeller. AzureHDInsightSecurityProfile</span><span class="sxs-lookup"><span data-stu-id="a9732-137">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightSecurityProfile</span></span>

## <span data-ttu-id="a9732-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a9732-138">NOTES</span></span>

## <span data-ttu-id="a9732-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a9732-139">RELATED LINKS</span></span>