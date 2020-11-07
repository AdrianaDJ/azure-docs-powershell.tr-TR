---
external help file: Microsoft.Azure.Commands.AnalysisServices.Dataplane.dll-Help.xml
Module Name: Azure.AnalysisServices
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Add-AzureAnalysisServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Add-AzureAnalysisServicesAccount.md
ms.openlocfilehash: 8b5133e62139fca02dc59f84e5fb714d2a35e675
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93765072"
---
# <span data-ttu-id="aa47e-101">Add-AzureAnalysisServicesAccount</span><span class="sxs-lookup"><span data-stu-id="aa47e-101">Add-AzureAnalysisServicesAccount</span></span>

## <span data-ttu-id="aa47e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aa47e-102">SYNOPSIS</span></span>
<span data-ttu-id="aa47e-103">Azure Analysis Services sunucu cmdlet istekleri için kullanılmak üzere kimliği doğrulanmış bir hesap ekler.</span><span class="sxs-lookup"><span data-stu-id="aa47e-103">Adds an authenticated account to use for Azure Analysis Services server cmdlet requests.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aa47e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="aa47e-104">SYNTAX</span></span>

### <span data-ttu-id="aa47e-105">UserParameterSetName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="aa47e-105">UserParameterSetName (Default)</span></span>
```
Add-AzureAnalysisServicesAccount [[-RolloutEnvironment] <String>] [[-Credential] <PSCredential>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aa47e-106">ServicePrincipalWithPasswordParameterSetName</span><span class="sxs-lookup"><span data-stu-id="aa47e-106">ServicePrincipalWithPasswordParameterSetName</span></span>
```
Add-AzureAnalysisServicesAccount [-RolloutEnvironment] <String> [-Credential] <PSCredential>
 [-ServicePrincipal] -TenantId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aa47e-107">ServicePrincipalWithCertificateParameterSetName</span><span class="sxs-lookup"><span data-stu-id="aa47e-107">ServicePrincipalWithCertificateParameterSetName</span></span>
```
Add-AzureAnalysisServicesAccount [-RolloutEnvironment] <String> [-ServicePrincipal] -TenantId <String>
 -ApplicationId <String> -CertificateThumbprint <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aa47e-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="aa47e-108">DESCRIPTION</span></span>
<span data-ttu-id="aa47e-109">Azure Analysis Services sunucusunda oturum açmak için Add-AzureAnalysisServicesAccount cmdlet 'i kullanılır</span><span class="sxs-lookup"><span data-stu-id="aa47e-109">The Add-AzureAnalysisServicesAccount cmdlet is used to login to an instance of Azure Analysis Services server</span></span>

## <span data-ttu-id="aa47e-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="aa47e-110">EXAMPLES</span></span>

### <span data-ttu-id="aa47e-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="aa47e-111">Example 1</span></span>
```
PS C:\>Add-AzureAnalysisServicesAccount
RolloutEnvironment: westcentralus.asazure.windows.net
Credential: $UserCredential
```

<span data-ttu-id="aa47e-112">Bu örnek, $UserCredential değişkeniyle belirtilen hesabı westcentralus.asazure.windows.net Analysis Services ortamına ekler.</span><span class="sxs-lookup"><span data-stu-id="aa47e-112">This example will add the account specified by the $UserCredential variable to the westcentralus.asazure.windows.net Analysis Services environment.</span></span>

### <span data-ttu-id="aa47e-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="aa47e-113">Example 2</span></span>
```
PS C:\>$ApplicationCredential = Get-Credential
PS C:\>Add-AzureAnalysisServicesAccount -RolloutEnvironment 'westcentralus.asazure.windows.net' -ServicePrincipal -Credential $ApplicationCredential -TenantId "xxxx-xxxx-xxxx-xxxx"
```

<span data-ttu-id="aa47e-114">İlk komut uygulama hizmeti sorumlusu kimlik bilgilerini alır ve $ApplicationCredential değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="aa47e-114">The first command gets the application service principal credentials, and then stores them in the $ApplicationCredential variable.</span></span>
<span data-ttu-id="aa47e-115">İkinci komut, $ApplicationCredential değişkeni ve Tenantıd tarafından belirtilen uygulama hizmeti Principal hesabını westcentralus.asazure.windows.net Analysis Services ortamına ekler.</span><span class="sxs-lookup"><span data-stu-id="aa47e-115">The second command add the application service principal account specified by the $ApplicationCredential variable and TenantId to the westcentralus.asazure.windows.net Analysis Services environment.</span></span>

### <span data-ttu-id="aa47e-116">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="aa47e-116">Example 3</span></span>
```
PS C:\>Add-AzureAnalysisServicesAccount -RolloutEnvironment 'westcentralus.asazure.windows.net' -ServicePrincipal -ApplicationId "yyyy-yyyy-yyyy-yyyy" -CertificateThumbprint 'zzzzzzzzzzzzzzzz' -TenantId "xxxx-xxxx-xxxx-xxxx"
```

<span data-ttu-id="aa47e-117">Bu örnek, ApplicationId, Tenantıd ve CertificateThumbprint tarafından belirtilen uygulama hizmeti sorumlu hesabını westcentralus.asazure.windows.net Analysis Services ortamına ekler.</span><span class="sxs-lookup"><span data-stu-id="aa47e-117">This example will add the application service principal account specified by the ApplicationId, TenantId and CertificateThumbprint to the westcentralus.asazure.windows.net Analysis Services environment.</span></span>

## <span data-ttu-id="aa47e-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="aa47e-118">PARAMETERS</span></span>

### <span data-ttu-id="aa47e-119">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="aa47e-119">-ApplicationId</span></span>
<span data-ttu-id="aa47e-120">Uygulama KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="aa47e-120">The application ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ServicePrincipalWithCertificateParameterSetName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa47e-121">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="aa47e-121">-CertificateThumbprint</span></span>
<span data-ttu-id="aa47e-122">Sertifika karması (Parmak Izi)</span><span class="sxs-lookup"><span data-stu-id="aa47e-122">Certificate Hash (Thumbprint)</span></span>

```yaml
Type: System.String
Parameter Sets: ServicePrincipalWithCertificateParameterSetName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa47e-123">-Credential</span><span class="sxs-lookup"><span data-stu-id="aa47e-123">-Credential</span></span>
<span data-ttu-id="aa47e-124">Oturum açma kimlik bilgileri</span><span class="sxs-lookup"><span data-stu-id="aa47e-124">Login credentials</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: UserParameterSetName
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: ServicePrincipalWithPasswordParameterSetName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa47e-125">-RolloutEnvironment</span><span class="sxs-lookup"><span data-stu-id="aa47e-125">-RolloutEnvironment</span></span>
<span data-ttu-id="aa47e-126">Oturum açılacak Azure Analysis Services ortamının adı.</span><span class="sxs-lookup"><span data-stu-id="aa47e-126">Name of the Azure Analysis Services environment to which to logon to.</span></span> <span data-ttu-id="aa47e-127">Asazure://westcentralus.asazure.windows.net/testserver sunucunun tam adı verildiğinde, bu değişken için doğru değer westcentralus.asazure.windows.net olur</span><span class="sxs-lookup"><span data-stu-id="aa47e-127">Given the full name of the server for example asazure://westcentralus.asazure.windows.net/testserver , the correct value for this variable will be westcentralus.asazure.windows.net</span></span>

```yaml
Type: System.String
Parameter Sets: UserParameterSetName
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ServicePrincipalWithPasswordParameterSetName, ServicePrincipalWithCertificateParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa47e-128">-ServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="aa47e-128">-ServicePrincipal</span></span>
<span data-ttu-id="aa47e-129">Bu hesabın, hizmet sorumlusu kimlik bilgilerini sağlayarak doğruladığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="aa47e-129">Indicates that this account authenticates by providing service principal credentials.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ServicePrincipalWithPasswordParameterSetName, ServicePrincipalWithCertificateParameterSetName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa47e-130">-Tenantıd</span><span class="sxs-lookup"><span data-stu-id="aa47e-130">-TenantId</span></span>
<span data-ttu-id="aa47e-131">Kiracı adı veya KIMLIĞI</span><span class="sxs-lookup"><span data-stu-id="aa47e-131">Tenant name or ID</span></span>

```yaml
Type: System.String
Parameter Sets: ServicePrincipalWithPasswordParameterSetName, ServicePrincipalWithCertificateParameterSetName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa47e-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="aa47e-132">-Confirm</span></span>
<span data-ttu-id="aa47e-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="aa47e-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aa47e-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa47e-134">-WhatIf</span></span>
<span data-ttu-id="aa47e-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="aa47e-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aa47e-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="aa47e-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aa47e-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa47e-137">CommonParameters</span></span>
<span data-ttu-id="aa47e-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="aa47e-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa47e-139">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aa47e-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa47e-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="aa47e-140">INPUTS</span></span>

## <span data-ttu-id="aa47e-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="aa47e-141">OUTPUTS</span></span>

### <span data-ttu-id="aa47e-142">Microsoft. Azure. Commands. AnalysisServices. Datadüzlemi. AsAzureProfile</span><span class="sxs-lookup"><span data-stu-id="aa47e-142">Microsoft.Azure.Commands.AnalysisServices.Dataplane.AsAzureProfile</span></span>

## <span data-ttu-id="aa47e-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="aa47e-143">NOTES</span></span>
<span data-ttu-id="aa47e-144">Diğer ad: Login-AzureAsAccount</span><span class="sxs-lookup"><span data-stu-id="aa47e-144">Alias: Login-AzureAsAccount</span></span>

## <span data-ttu-id="aa47e-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="aa47e-145">RELATED LINKS</span></span>

