---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/stop-azspringcloudappdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Stop-AzSpringCloudAppDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Stop-AzSpringCloudAppDeployment.md
ms.openlocfilehash: 3f98161e56019394dc67ab8909aac3fb70a611a2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94275225"
---
# <span data-ttu-id="1cc41-101">Stop-AzSpringCloudAppDeployment</span><span class="sxs-lookup"><span data-stu-id="1cc41-101">Stop-AzSpringCloudAppDeployment</span></span>

## <span data-ttu-id="1cc41-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1cc41-102">SYNOPSIS</span></span>
<span data-ttu-id="1cc41-103">Dağıtımı durdurun.</span><span class="sxs-lookup"><span data-stu-id="1cc41-103">Stop the deployment.</span></span>

## <span data-ttu-id="1cc41-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1cc41-104">SYNTAX</span></span>

### <span data-ttu-id="1cc41-105">Durdur (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="1cc41-105">Stop (Default)</span></span>
```
Stop-AzSpringCloudAppDeployment -AppName <String> -Name <String> -ResourceGroupName <String>
 -ServiceName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="1cc41-106">Stopviaıdentity</span><span class="sxs-lookup"><span data-stu-id="1cc41-106">StopViaIdentity</span></span>
```
Stop-AzSpringCloudAppDeployment -InputObject <ISpringCloudIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="1cc41-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="1cc41-107">DESCRIPTION</span></span>
<span data-ttu-id="1cc41-108">Dağıtımı durdurun.</span><span class="sxs-lookup"><span data-stu-id="1cc41-108">Stop the deployment.</span></span>

## <span data-ttu-id="1cc41-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1cc41-109">EXAMPLES</span></span>

### <span data-ttu-id="1cc41-110">Örnek 1: bir bulut hizmetini adıyla durdurun.</span><span class="sxs-lookup"><span data-stu-id="1cc41-110">Example 1: Stop Spring Cloud Service by name.</span></span>
```powershell
PS C:\> Stop-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway -DeploymentName default
```

<span data-ttu-id="1cc41-111">Yay bulut hizmetini adıyla durdurun.</span><span class="sxs-lookup"><span data-stu-id="1cc41-111">Stop Spring Cloud Service by name.</span></span>

### <span data-ttu-id="1cc41-112">Örnek 2: bir bulut hizmeti 'ni kanaldan durdurun.</span><span class="sxs-lookup"><span data-stu-id="1cc41-112">Example 2: Stop Spring Cloud Service from pipe.</span></span>
```powershell
PS C:\> Get-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway -DeploymentName default | Stop-AzSpringCloud
```

<span data-ttu-id="1cc41-113">Yay bulut hizmetini kanaldan durdurun.</span><span class="sxs-lookup"><span data-stu-id="1cc41-113">Stop Spring Cloud Service from pipe.</span></span>

## <span data-ttu-id="1cc41-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1cc41-114">PARAMETERS</span></span>

### <span data-ttu-id="1cc41-115">-AppName</span><span class="sxs-lookup"><span data-stu-id="1cc41-115">-AppName</span></span>
<span data-ttu-id="1cc41-116">Uygulama kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="1cc41-116">The name of the App resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Stop
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1cc41-117">-Iş</span><span class="sxs-lookup"><span data-stu-id="1cc41-117">-AsJob</span></span>
<span data-ttu-id="1cc41-118">Komutu iş olarak çalıştırmak</span><span class="sxs-lookup"><span data-stu-id="1cc41-118">Run the command as a job</span></span>

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

### <span data-ttu-id="1cc41-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1cc41-119">-DefaultProfile</span></span>
<span data-ttu-id="1cc41-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1cc41-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1cc41-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1cc41-121">-InputObject</span></span>
<span data-ttu-id="1cc41-122">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1cc41-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity
Parameter Sets: StopViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1cc41-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="1cc41-123">-Name</span></span>
<span data-ttu-id="1cc41-124">Dağıtım kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="1cc41-124">The name of the Deployment resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Stop
Aliases: DeploymentName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1cc41-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="1cc41-125">-NoWait</span></span>
<span data-ttu-id="1cc41-126">Komutu zaman uyumsuz olarak çalıştırır</span><span class="sxs-lookup"><span data-stu-id="1cc41-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="1cc41-127">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="1cc41-127">-PassThru</span></span>
<span data-ttu-id="1cc41-128">Komut başarılı olduğunda doğru verir</span><span class="sxs-lookup"><span data-stu-id="1cc41-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="1cc41-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1cc41-129">-ResourceGroupName</span></span>
<span data-ttu-id="1cc41-130">Kaynağı içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="1cc41-130">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="1cc41-131">Bu değeri Azure Resource Manager API 'dan veya portalınızdan edinebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1cc41-131">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: Stop
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1cc41-132">-HizmetAdı</span><span class="sxs-lookup"><span data-stu-id="1cc41-132">-ServiceName</span></span>
<span data-ttu-id="1cc41-133">Hizmet kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="1cc41-133">The name of the Service resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Stop
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1cc41-134">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="1cc41-134">-SubscriptionId</span></span>
<span data-ttu-id="1cc41-135">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik KIMLIĞINI alır.</span><span class="sxs-lookup"><span data-stu-id="1cc41-135">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="1cc41-136">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="1cc41-136">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Stop
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1cc41-137">-Onay</span><span class="sxs-lookup"><span data-stu-id="1cc41-137">-Confirm</span></span>
<span data-ttu-id="1cc41-138">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="1cc41-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1cc41-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1cc41-139">-WhatIf</span></span>
<span data-ttu-id="1cc41-140">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1cc41-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1cc41-141">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="1cc41-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1cc41-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1cc41-142">CommonParameters</span></span>
<span data-ttu-id="1cc41-143">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1cc41-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1cc41-144">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="1cc41-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1cc41-145">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1cc41-145">INPUTS</span></span>

### <span data-ttu-id="1cc41-146">Microsoft. Azure. PowerShell. cmdlet. SpringCloud. modeller. ıspringcloudidentity</span><span class="sxs-lookup"><span data-stu-id="1cc41-146">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="1cc41-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1cc41-147">OUTPUTS</span></span>

### <span data-ttu-id="1cc41-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1cc41-148">System.Boolean</span></span>

## <span data-ttu-id="1cc41-149">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1cc41-149">NOTES</span></span>

<span data-ttu-id="1cc41-150">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="1cc41-150">ALIASES</span></span>

<span data-ttu-id="1cc41-151">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="1cc41-151">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="1cc41-152">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="1cc41-152">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1cc41-153">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="1cc41-153">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="1cc41-154">INPUTOBJECT <ISpringCloudIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="1cc41-154">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="1cc41-155">`[AppName <String>]`: Uygulama kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="1cc41-155">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="1cc41-156">`[BindingName <String>]`: Bağlama kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="1cc41-156">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="1cc41-157">`[CertificateName <String>]`: Sertifika kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="1cc41-157">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="1cc41-158">`[DeploymentName <String>]`: Dağıtım kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="1cc41-158">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="1cc41-159">`[DomainName <String>]`: Özel etki alanı kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="1cc41-159">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="1cc41-160">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="1cc41-160">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="1cc41-161">`[Location <String>]`: bölge</span><span class="sxs-lookup"><span data-stu-id="1cc41-161">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="1cc41-162">`[ResourceGroupName <String>]`: Kaynağı içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="1cc41-162">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="1cc41-163">Bu değeri Azure Resource Manager API 'dan veya portalınızdan edinebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1cc41-163">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="1cc41-164">`[ServiceName <String>]`: Hizmet kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="1cc41-164">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="1cc41-165">`[SubscriptionId <String>]`: Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik KIMLIĞINI alır.</span><span class="sxs-lookup"><span data-stu-id="1cc41-165">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="1cc41-166">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="1cc41-166">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="1cc41-167">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1cc41-167">RELATED LINKS</span></span>

