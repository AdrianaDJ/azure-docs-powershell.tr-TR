---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/remove-azspringcloudappdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Remove-AzSpringCloudAppDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Remove-AzSpringCloudAppDeployment.md
ms.openlocfilehash: f91747d7c48521a9a14906cd873df564fadc4aa7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94110262"
---
# <span data-ttu-id="bf31e-101">Remove-AzSpringCloudAppDeployment</span><span class="sxs-lookup"><span data-stu-id="bf31e-101">Remove-AzSpringCloudAppDeployment</span></span>

## <span data-ttu-id="bf31e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bf31e-102">SYNOPSIS</span></span>
<span data-ttu-id="bf31e-103">Bir dağıtımı silme işlemi.</span><span class="sxs-lookup"><span data-stu-id="bf31e-103">Operation to delete a Deployment.</span></span>

## <span data-ttu-id="bf31e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bf31e-104">SYNTAX</span></span>

### <span data-ttu-id="bf31e-105">Sil (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="bf31e-105">Delete (Default)</span></span>
```
Remove-AzSpringCloudAppDeployment -AppName <String> -Name <String> -ResourceGroupName <String>
 -ServiceName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="bf31e-106">Deleteviaıdentity</span><span class="sxs-lookup"><span data-stu-id="bf31e-106">DeleteViaIdentity</span></span>
```
Remove-AzSpringCloudAppDeployment -InputObject <ISpringCloudIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="bf31e-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="bf31e-107">DESCRIPTION</span></span>
<span data-ttu-id="bf31e-108">Bir dağıtımı silme işlemi.</span><span class="sxs-lookup"><span data-stu-id="bf31e-108">Operation to delete a Deployment.</span></span>

## <span data-ttu-id="bf31e-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bf31e-109">EXAMPLES</span></span>

### <span data-ttu-id="bf31e-110">Örnek 1: yay bulut dağıtımını ada göre kaldır.</span><span class="sxs-lookup"><span data-stu-id="bf31e-110">Example 1: Remove Spring Cloud Deployment by name.</span></span>
```powershell
PS C:\> Remove-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway -DeploymentName default
```

<span data-ttu-id="bf31e-111">Yay bulut dağıtımını ada göre kaldır.</span><span class="sxs-lookup"><span data-stu-id="bf31e-111">Remove Spring Cloud Deployment by name.</span></span>

### <span data-ttu-id="bf31e-112">Örnek 2: yay bulut dağıtımını kanaldan kaldır.</span><span class="sxs-lookup"><span data-stu-id="bf31e-112">Example 2: Remove Spring Cloud Deployment from pipe.</span></span>
```powershell
PS C:\> Get-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway -DeploymentName default | Remove-AzSpringCloudAppDeployment
```

<span data-ttu-id="bf31e-113">Yay bulut dağıtımını kanaldan kaldır.</span><span class="sxs-lookup"><span data-stu-id="bf31e-113">Remove Spring Cloud Deployment from pipe.</span></span>

## <span data-ttu-id="bf31e-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bf31e-114">PARAMETERS</span></span>

### <span data-ttu-id="bf31e-115">-AppName</span><span class="sxs-lookup"><span data-stu-id="bf31e-115">-AppName</span></span>
<span data-ttu-id="bf31e-116">Uygulama kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="bf31e-116">The name of the App resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf31e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf31e-117">-DefaultProfile</span></span>
<span data-ttu-id="bf31e-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="bf31e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf31e-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bf31e-119">-InputObject</span></span>
<span data-ttu-id="bf31e-120">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="bf31e-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bf31e-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="bf31e-121">-Name</span></span>
<span data-ttu-id="bf31e-122">Dağıtım kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="bf31e-122">The name of the Deployment resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: DeploymentName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf31e-123">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="bf31e-123">-PassThru</span></span>
<span data-ttu-id="bf31e-124">Komut başarılı olduğunda doğru verir</span><span class="sxs-lookup"><span data-stu-id="bf31e-124">Returns true when the command succeeds</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf31e-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf31e-125">-ResourceGroupName</span></span>
<span data-ttu-id="bf31e-126">Kaynağı içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="bf31e-126">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="bf31e-127">Bu değeri Azure Resource Manager API 'dan veya portalınızdan edinebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="bf31e-127">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf31e-128">-HizmetAdı</span><span class="sxs-lookup"><span data-stu-id="bf31e-128">-ServiceName</span></span>
<span data-ttu-id="bf31e-129">Hizmet kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="bf31e-129">The name of the Service resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf31e-130">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="bf31e-130">-SubscriptionId</span></span>
<span data-ttu-id="bf31e-131">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik KIMLIĞINI alır.</span><span class="sxs-lookup"><span data-stu-id="bf31e-131">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="bf31e-132">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="bf31e-132">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf31e-133">-Onay</span><span class="sxs-lookup"><span data-stu-id="bf31e-133">-Confirm</span></span>
<span data-ttu-id="bf31e-134">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="bf31e-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bf31e-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bf31e-135">-WhatIf</span></span>
<span data-ttu-id="bf31e-136">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="bf31e-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bf31e-137">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="bf31e-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bf31e-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf31e-138">CommonParameters</span></span>
<span data-ttu-id="bf31e-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bf31e-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf31e-140">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="bf31e-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf31e-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bf31e-141">INPUTS</span></span>

### <span data-ttu-id="bf31e-142">Microsoft. Azure. PowerShell. cmdlet. SpringCloud. modeller. ıspringcloudidentity</span><span class="sxs-lookup"><span data-stu-id="bf31e-142">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="bf31e-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bf31e-143">OUTPUTS</span></span>

### <span data-ttu-id="bf31e-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="bf31e-144">System.Boolean</span></span>

## <span data-ttu-id="bf31e-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bf31e-145">NOTES</span></span>

<span data-ttu-id="bf31e-146">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="bf31e-146">ALIASES</span></span>

<span data-ttu-id="bf31e-147">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="bf31e-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="bf31e-148">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="bf31e-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="bf31e-149">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="bf31e-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="bf31e-150">INPUTOBJECT <ISpringCloudIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="bf31e-150">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="bf31e-151">`[AppName <String>]`: Uygulama kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="bf31e-151">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="bf31e-152">`[BindingName <String>]`: Bağlama kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="bf31e-152">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="bf31e-153">`[CertificateName <String>]`: Sertifika kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="bf31e-153">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="bf31e-154">`[DeploymentName <String>]`: Dağıtım kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="bf31e-154">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="bf31e-155">`[DomainName <String>]`: Özel etki alanı kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="bf31e-155">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="bf31e-156">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="bf31e-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="bf31e-157">`[Location <String>]`: bölge</span><span class="sxs-lookup"><span data-stu-id="bf31e-157">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="bf31e-158">`[ResourceGroupName <String>]`: Kaynağı içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="bf31e-158">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="bf31e-159">Bu değeri Azure Resource Manager API 'dan veya portalınızdan edinebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="bf31e-159">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="bf31e-160">`[ServiceName <String>]`: Hizmet kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="bf31e-160">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="bf31e-161">`[SubscriptionId <String>]`: Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik KIMLIĞINI alır.</span><span class="sxs-lookup"><span data-stu-id="bf31e-161">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="bf31e-162">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="bf31e-162">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="bf31e-163">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bf31e-163">RELATED LINKS</span></span>

