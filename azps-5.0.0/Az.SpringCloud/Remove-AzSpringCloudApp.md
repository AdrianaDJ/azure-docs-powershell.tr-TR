---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/remove-azspringcloudapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Remove-AzSpringCloudApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Remove-AzSpringCloudApp.md
ms.openlocfilehash: e363a7bedc891c736f06b60c093483010e6b261d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94275227"
---
# <span data-ttu-id="ba18d-101">Remove-AzSpringCloudApp</span><span class="sxs-lookup"><span data-stu-id="ba18d-101">Remove-AzSpringCloudApp</span></span>

## <span data-ttu-id="ba18d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ba18d-102">SYNOPSIS</span></span>
<span data-ttu-id="ba18d-103">Uygulamayı silme işlemi.</span><span class="sxs-lookup"><span data-stu-id="ba18d-103">Operation to delete an App.</span></span>

## <span data-ttu-id="ba18d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ba18d-104">SYNTAX</span></span>

### <span data-ttu-id="ba18d-105">Sil (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="ba18d-105">Delete (Default)</span></span>
```
Remove-AzSpringCloudApp -Name <String> -ResourceGroupName <String> -ServiceName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="ba18d-106">Deleteviaıdentity</span><span class="sxs-lookup"><span data-stu-id="ba18d-106">DeleteViaIdentity</span></span>
```
Remove-AzSpringCloudApp -InputObject <ISpringCloudIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ba18d-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="ba18d-107">DESCRIPTION</span></span>
<span data-ttu-id="ba18d-108">Uygulamayı silme işlemi.</span><span class="sxs-lookup"><span data-stu-id="ba18d-108">Operation to delete an App.</span></span>

## <span data-ttu-id="ba18d-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ba18d-109">EXAMPLES</span></span>

### <span data-ttu-id="ba18d-110">Örnek 1: yay bulut uygulamasını ada göre kaldır.</span><span class="sxs-lookup"><span data-stu-id="ba18d-110">Example 1: Remove Spring Cloud App by name.</span></span>
```powershell
PS C:\> Remove-AzSpringCloudApp -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway
```

<span data-ttu-id="ba18d-111">Yay bulut uygulamasını ada göre kaldır.</span><span class="sxs-lookup"><span data-stu-id="ba18d-111">Remove Spring Cloud App by name.</span></span>

### <span data-ttu-id="ba18d-112">Örnek 2: yay bulut uygulamasını kanaldan kaldır.</span><span class="sxs-lookup"><span data-stu-id="ba18d-112">Example 2: Remove Spring Cloud App from pipe.</span></span>
```powershell
PS C:\> Get-AzSpringCloudApp -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway | Remove-AzSpringCloudApp
```

<span data-ttu-id="ba18d-113">Yay bulut uygulamasını kanaldan kaldır.</span><span class="sxs-lookup"><span data-stu-id="ba18d-113">Remove Spring Cloud App from pipe.</span></span>

## <span data-ttu-id="ba18d-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ba18d-114">PARAMETERS</span></span>

### <span data-ttu-id="ba18d-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="ba18d-115">-AsJob</span></span>
<span data-ttu-id="ba18d-116">Komutu iş olarak çalıştırmak</span><span class="sxs-lookup"><span data-stu-id="ba18d-116">Run the command as a job</span></span>

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

### <span data-ttu-id="ba18d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba18d-117">-DefaultProfile</span></span>
<span data-ttu-id="ba18d-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ba18d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ba18d-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ba18d-119">-InputObject</span></span>
<span data-ttu-id="ba18d-120">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ba18d-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="ba18d-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="ba18d-121">-Name</span></span>
<span data-ttu-id="ba18d-122">Uygulama kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="ba18d-122">The name of the App resource.</span></span>

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

### <span data-ttu-id="ba18d-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="ba18d-123">-NoWait</span></span>
<span data-ttu-id="ba18d-124">Komutu zaman uyumsuz olarak çalıştırır</span><span class="sxs-lookup"><span data-stu-id="ba18d-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="ba18d-125">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="ba18d-125">-PassThru</span></span>
<span data-ttu-id="ba18d-126">Komut başarılı olduğunda doğru verir</span><span class="sxs-lookup"><span data-stu-id="ba18d-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="ba18d-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba18d-127">-ResourceGroupName</span></span>
<span data-ttu-id="ba18d-128">Kaynağı içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="ba18d-128">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="ba18d-129">Bu değeri Azure Resource Manager API 'dan veya portalınızdan edinebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ba18d-129">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="ba18d-130">-HizmetAdı</span><span class="sxs-lookup"><span data-stu-id="ba18d-130">-ServiceName</span></span>
<span data-ttu-id="ba18d-131">Hizmet kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="ba18d-131">The name of the Service resource.</span></span>

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

### <span data-ttu-id="ba18d-132">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="ba18d-132">-SubscriptionId</span></span>
<span data-ttu-id="ba18d-133">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik KIMLIĞINI alır.</span><span class="sxs-lookup"><span data-stu-id="ba18d-133">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="ba18d-134">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="ba18d-134">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="ba18d-135">-Onay</span><span class="sxs-lookup"><span data-stu-id="ba18d-135">-Confirm</span></span>
<span data-ttu-id="ba18d-136">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ba18d-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ba18d-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba18d-137">-WhatIf</span></span>
<span data-ttu-id="ba18d-138">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ba18d-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ba18d-139">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ba18d-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ba18d-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba18d-140">CommonParameters</span></span>
<span data-ttu-id="ba18d-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ba18d-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba18d-142">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="ba18d-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba18d-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ba18d-143">INPUTS</span></span>

### <span data-ttu-id="ba18d-144">Microsoft. Azure. PowerShell. cmdlet. SpringCloud. modeller. ıspringcloudidentity</span><span class="sxs-lookup"><span data-stu-id="ba18d-144">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="ba18d-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ba18d-145">OUTPUTS</span></span>

### <span data-ttu-id="ba18d-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ba18d-146">System.Boolean</span></span>

## <span data-ttu-id="ba18d-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ba18d-147">NOTES</span></span>

<span data-ttu-id="ba18d-148">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="ba18d-148">ALIASES</span></span>

<span data-ttu-id="ba18d-149">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="ba18d-149">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ba18d-150">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="ba18d-150">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ba18d-151">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ba18d-151">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ba18d-152">INPUTOBJECT <ISpringCloudIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="ba18d-152">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ba18d-153">`[AppName <String>]`: Uygulama kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="ba18d-153">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="ba18d-154">`[BindingName <String>]`: Bağlama kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="ba18d-154">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="ba18d-155">`[CertificateName <String>]`: Sertifika kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="ba18d-155">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="ba18d-156">`[DeploymentName <String>]`: Dağıtım kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="ba18d-156">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="ba18d-157">`[DomainName <String>]`: Özel etki alanı kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="ba18d-157">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="ba18d-158">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="ba18d-158">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ba18d-159">`[Location <String>]`: bölge</span><span class="sxs-lookup"><span data-stu-id="ba18d-159">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="ba18d-160">`[ResourceGroupName <String>]`: Kaynağı içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="ba18d-160">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="ba18d-161">Bu değeri Azure Resource Manager API 'dan veya portalınızdan edinebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ba18d-161">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="ba18d-162">`[ServiceName <String>]`: Hizmet kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="ba18d-162">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="ba18d-163">`[SubscriptionId <String>]`: Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik KIMLIĞINI alır.</span><span class="sxs-lookup"><span data-stu-id="ba18d-163">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="ba18d-164">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="ba18d-164">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="ba18d-165">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ba18d-165">RELATED LINKS</span></span>

