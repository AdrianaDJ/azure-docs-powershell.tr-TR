---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/remove-azspringcloudapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Remove-AzSpringCloudApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Remove-AzSpringCloudApp.md
ms.openlocfilehash: ace761bfd329c756baa27d1bff6300f2e030f377
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94273928"
---
# <span data-ttu-id="27a26-101">Remove-AzSpringCloudApp</span><span class="sxs-lookup"><span data-stu-id="27a26-101">Remove-AzSpringCloudApp</span></span>

## <span data-ttu-id="27a26-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="27a26-102">SYNOPSIS</span></span>
<span data-ttu-id="27a26-103">Uygulamayı silme işlemi.</span><span class="sxs-lookup"><span data-stu-id="27a26-103">Operation to delete an App.</span></span>

## <span data-ttu-id="27a26-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="27a26-104">SYNTAX</span></span>

### <span data-ttu-id="27a26-105">Sil (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="27a26-105">Delete (Default)</span></span>
```
Remove-AzSpringCloudApp -Name <String> -ResourceGroupName <String> -ServiceName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="27a26-106">Deleteviaıdentity</span><span class="sxs-lookup"><span data-stu-id="27a26-106">DeleteViaIdentity</span></span>
```
Remove-AzSpringCloudApp -InputObject <ISpringCloudIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="27a26-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="27a26-107">DESCRIPTION</span></span>
<span data-ttu-id="27a26-108">Uygulamayı silme işlemi.</span><span class="sxs-lookup"><span data-stu-id="27a26-108">Operation to delete an App.</span></span>

## <span data-ttu-id="27a26-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="27a26-109">EXAMPLES</span></span>

### <span data-ttu-id="27a26-110">Örnek 1: yay bulut uygulamasını ada göre kaldır.</span><span class="sxs-lookup"><span data-stu-id="27a26-110">Example 1: Remove Spring Cloud App by name.</span></span>
```powershell
PS C:\> Remove-AzSpringCloudApp -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway
```

<span data-ttu-id="27a26-111">Yay bulut uygulamasını ada göre kaldır.</span><span class="sxs-lookup"><span data-stu-id="27a26-111">Remove Spring Cloud App by name.</span></span>

### <span data-ttu-id="27a26-112">Örnek 2: yay bulut uygulamasını kanaldan kaldır.</span><span class="sxs-lookup"><span data-stu-id="27a26-112">Example 2: Remove Spring Cloud App from pipe.</span></span>
```powershell
PS C:\> Get-AzSpringCloudApp -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway | Remove-AzSpringCloudApp
```

<span data-ttu-id="27a26-113">Yay bulut uygulamasını kanaldan kaldır.</span><span class="sxs-lookup"><span data-stu-id="27a26-113">Remove Spring Cloud App from pipe.</span></span>

## <span data-ttu-id="27a26-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="27a26-114">PARAMETERS</span></span>

### <span data-ttu-id="27a26-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27a26-115">-DefaultProfile</span></span>
<span data-ttu-id="27a26-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="27a26-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="27a26-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="27a26-117">-InputObject</span></span>
<span data-ttu-id="27a26-118">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="27a26-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="27a26-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="27a26-119">-Name</span></span>
<span data-ttu-id="27a26-120">Uygulama kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="27a26-120">The name of the App resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: AppName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27a26-121">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="27a26-121">-PassThru</span></span>
<span data-ttu-id="27a26-122">Komut başarılı olduğunda doğru verir</span><span class="sxs-lookup"><span data-stu-id="27a26-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="27a26-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27a26-123">-ResourceGroupName</span></span>
<span data-ttu-id="27a26-124">Kaynağı içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="27a26-124">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="27a26-125">Bu değeri Azure Resource Manager API 'dan veya portalınızdan edinebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="27a26-125">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="27a26-126">-HizmetAdı</span><span class="sxs-lookup"><span data-stu-id="27a26-126">-ServiceName</span></span>
<span data-ttu-id="27a26-127">Hizmet kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="27a26-127">The name of the Service resource.</span></span>

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

### <span data-ttu-id="27a26-128">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="27a26-128">-SubscriptionId</span></span>
<span data-ttu-id="27a26-129">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik KIMLIĞINI alır.</span><span class="sxs-lookup"><span data-stu-id="27a26-129">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="27a26-130">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="27a26-130">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="27a26-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="27a26-131">-Confirm</span></span>
<span data-ttu-id="27a26-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="27a26-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="27a26-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27a26-133">-WhatIf</span></span>
<span data-ttu-id="27a26-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="27a26-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="27a26-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="27a26-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="27a26-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27a26-136">CommonParameters</span></span>
<span data-ttu-id="27a26-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="27a26-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27a26-138">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="27a26-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27a26-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="27a26-139">INPUTS</span></span>

### <span data-ttu-id="27a26-140">Microsoft. Azure. PowerShell. cmdlet. SpringCloud. modeller. ıspringcloudidentity</span><span class="sxs-lookup"><span data-stu-id="27a26-140">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="27a26-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="27a26-141">OUTPUTS</span></span>

### <span data-ttu-id="27a26-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="27a26-142">System.Boolean</span></span>

## <span data-ttu-id="27a26-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="27a26-143">NOTES</span></span>

<span data-ttu-id="27a26-144">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="27a26-144">ALIASES</span></span>

<span data-ttu-id="27a26-145">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="27a26-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="27a26-146">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="27a26-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="27a26-147">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="27a26-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="27a26-148">INPUTOBJECT <ISpringCloudIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="27a26-148">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="27a26-149">`[AppName <String>]`: Uygulama kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="27a26-149">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="27a26-150">`[BindingName <String>]`: Bağlama kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="27a26-150">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="27a26-151">`[CertificateName <String>]`: Sertifika kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="27a26-151">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="27a26-152">`[DeploymentName <String>]`: Dağıtım kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="27a26-152">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="27a26-153">`[DomainName <String>]`: Özel etki alanı kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="27a26-153">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="27a26-154">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="27a26-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="27a26-155">`[Location <String>]`: bölge</span><span class="sxs-lookup"><span data-stu-id="27a26-155">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="27a26-156">`[ResourceGroupName <String>]`: Kaynağı içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="27a26-156">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="27a26-157">Bu değeri Azure Resource Manager API 'dan veya portalınızdan edinebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="27a26-157">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="27a26-158">`[ServiceName <String>]`: Hizmet kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="27a26-158">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="27a26-159">`[SubscriptionId <String>]`: Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik KIMLIĞINI alır.</span><span class="sxs-lookup"><span data-stu-id="27a26-159">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="27a26-160">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="27a26-160">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="27a26-161">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="27a26-161">RELATED LINKS</span></span>

