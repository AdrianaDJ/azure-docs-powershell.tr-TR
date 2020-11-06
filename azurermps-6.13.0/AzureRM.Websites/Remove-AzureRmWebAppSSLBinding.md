---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 3AB3D398-E5DB-4214-BA27-6E3B7D225550
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/remove-azurermwebappsslbinding
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmWebAppSSLBinding.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmWebAppSSLBinding.md
ms.openlocfilehash: 52e5dce154b6798a0bddb0416235d371d6c85910
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590789"
---
# <span data-ttu-id="4ec50-101">Remove-AzureRmWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="4ec50-101">Remove-AzureRmWebAppSSLBinding</span></span>

## <span data-ttu-id="4ec50-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4ec50-102">SYNOPSIS</span></span>
<span data-ttu-id="4ec50-103">Karşıya yüklenen sertifikadan SSL bağlamasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="4ec50-103">Removes an SSL binding from an uploaded certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4ec50-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4ec50-104">SYNTAX</span></span>

### <span data-ttu-id="4ec50-105">S1</span><span class="sxs-lookup"><span data-stu-id="4ec50-105">S1</span></span>
```
Remove-AzureRmWebAppSSLBinding [-Name] <String> [[-DeleteCertificate] <Boolean>] [-Force]
 [-ResourceGroupName] <String> [-WebAppName] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4ec50-106">S2</span><span class="sxs-lookup"><span data-stu-id="4ec50-106">S2</span></span>
```
Remove-AzureRmWebAppSSLBinding [-Name] <String> [[-DeleteCertificate] <Boolean>] [-Force] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4ec50-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="4ec50-107">DESCRIPTION</span></span>
<span data-ttu-id="4ec50-108">**Remove-AzureRmWebAppSSLBinding** cmdlet 'i, bir Azure Web uygulamasından güvenli yuva KATMANı (SSL) bağlamasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="4ec50-108">The **Remove-AzureRmWebAppSSLBinding** cmdlet removes a Secure Sockets Layer (SSL) binding from an Azure Web App.</span></span>
<span data-ttu-id="4ec50-109">SSL bağlamaları bir Web uygulamasını sertifikayla ilişkilendirmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="4ec50-109">SSL bindings are used to associate a Web App with a certificate.</span></span>

## <span data-ttu-id="4ec50-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4ec50-110">EXAMPLES</span></span>

### <span data-ttu-id="4ec50-111">Örnek 1: Web uygulamasının SSL bağlamasını kaldırma</span><span class="sxs-lookup"><span data-stu-id="4ec50-111">Example 1: Remove an SSL binding for a web app</span></span>
```
PS C:\>Remove-AzureRmWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp" -Name "www.contoso.com"
```

<span data-ttu-id="4ec50-112">Bu komut, Web uygulamasının ContosoWebApp için SSL bağlamasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="4ec50-112">This command removes the SSL binding for the web app ContosoWebApp.</span></span>
<span data-ttu-id="4ec50-113">*Deletecertificate* parametresi dahil olmadığından, SERTIFIKA artık SSL bağlamaları yoksa silinir.</span><span class="sxs-lookup"><span data-stu-id="4ec50-113">Since the *DeleteCertificate* parameter is not included, the certificate will be deleted if it no longer has any SSL bindings.</span></span>

### <span data-ttu-id="4ec50-114">Örnek 2: sertifikayı kaldırmadan SSL bağlamasını kaldırma</span><span class="sxs-lookup"><span data-stu-id="4ec50-114">Example 2: Remove an SSL binding without removing the certificate</span></span>
```
PS C:\>Remove-AzureRmWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp" -Name "www.contoso.com" -DeleteCertificate $False
```

<span data-ttu-id="4ec50-115">Bu komut, örnek 1 ' e benzer şekilde, Web uygulamasının ContosoWebApp için SSL bağlamasını da kaldırır.</span><span class="sxs-lookup"><span data-stu-id="4ec50-115">Similar to Example 1, this command also removes the SSL binding for the Web App ContosoWebApp.</span></span>
<span data-ttu-id="4ec50-116">Bu örnekte, *Deletecertificate* parametresi eklenir ve parametre değeri $false olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="4ec50-116">In this case, however, the *DeleteCertificate* parameter is included, and the parameter value is set to $False.</span></span>
<span data-ttu-id="4ec50-117">Bu, herhangi bir SSL bağlaması olup olmamasına bakılmaksızın sertifikanın silinmeyeceği anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="4ec50-117">That means that the certificate will not be deleted regardless of whether it has any SSL bindings or not.</span></span>

### <span data-ttu-id="4ec50-118">Örnek 3: SSL bağlamasını kaldırmak için nesne başvurusu kullanma</span><span class="sxs-lookup"><span data-stu-id="4ec50-118">Example 3: Use an object reference to remove an SSL binding</span></span>
```
PS C:\>$WebApp = Get-AzureRmWebApp -Name "ContosoWebApp"
PS C:\> Remove-AzureRmWebAppSSLBinding -WebApp $WebApp -Name "www.contoso.com"
```

<span data-ttu-id="4ec50-119">Bu örnekte, Web uygulamasının SSL bağlamasını kaldırmak için Web App Web sitesinin nesne başvurusu kullanılır.</span><span class="sxs-lookup"><span data-stu-id="4ec50-119">This example uses an object reference to the Web App website to remove the SSL binding for a Web App.</span></span>
<span data-ttu-id="4ec50-120">İlk komut, Get-AzureRmWebApp cmdlet 'ini kullanarak, ContosoWebApp adlı Web uygulamasına nesne başvurusu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4ec50-120">The first command uses the Get-AzureRmWebApp cmdlet to create an object reference to the Web App named ContosoWebApp.</span></span>
<span data-ttu-id="4ec50-121">Bu nesne başvurusu $WebApp adlı bir değişkende depolanır.</span><span class="sxs-lookup"><span data-stu-id="4ec50-121">That object reference is stored in a variable named $WebApp.</span></span>
<span data-ttu-id="4ec50-122">İkinci komut, SSL bağlamasını kaldırmak için nesne başvurusu ve **Remove-AzureRmWebAppSSLBinding** cmdlet 'ini kullanır.</span><span class="sxs-lookup"><span data-stu-id="4ec50-122">The second command uses the object reference and the **Remove-AzureRmWebAppSSLBinding** cmdlet to remove the SSL binding.</span></span>

## <span data-ttu-id="4ec50-123">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4ec50-123">PARAMETERS</span></span>

### <span data-ttu-id="4ec50-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ec50-124">-DefaultProfile</span></span>
<span data-ttu-id="4ec50-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4ec50-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4ec50-126">-DeleteCertificate</span><span class="sxs-lookup"><span data-stu-id="4ec50-126">-DeleteCertificate</span></span>
<span data-ttu-id="4ec50-127">Kaldırılan SSL bağlaması sertifika tarafından kullanılan tek bağlamadır, gerçekleşecek eylemi belirtir.</span><span class="sxs-lookup"><span data-stu-id="4ec50-127">Specifies the action to take place if the SSL binding being removed is the only binding used by the certificate.</span></span>
<span data-ttu-id="4ec50-128">*Deletecertificate* $false olarak ayarlanırsa, bağlama silindiğinde sertifika silinmez.</span><span class="sxs-lookup"><span data-stu-id="4ec50-128">If *DeleteCertificate* is set to $False, the certificate will not be deleted when the binding is deleted.</span></span>
<span data-ttu-id="4ec50-129">*Deletecertificate* $true olarak ayarlanmışsa veya komuta dahil değilse, sertifika SSL bağlamasıyla birlikte silinir.</span><span class="sxs-lookup"><span data-stu-id="4ec50-129">If *DeleteCertificate* is set to $True or is not included in the command, the certificate will be deleted along with the SSL binding.</span></span>
<span data-ttu-id="4ec50-130">Sertifika yalnızca kaldırılan SSL bağlaması sertifika tarafından kullanılan tek bağlamadır silinir.</span><span class="sxs-lookup"><span data-stu-id="4ec50-130">The certificate will only be deleted if the SSL binding being removed is the only binding used by the certificate.</span></span>
<span data-ttu-id="4ec50-131">Sertifikada birden fazla bağlama varsa, sertifika *deletecertificate* parametresinin değerinden bağımsız olarak kaldırılamaz.</span><span class="sxs-lookup"><span data-stu-id="4ec50-131">If the certificate has more than one binding, the certificate will not be removed regardless of the value of the *DeleteCertificate* parameter.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ec50-132">-Force</span><span class="sxs-lookup"><span data-stu-id="4ec50-132">-Force</span></span>
<span data-ttu-id="4ec50-133">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="4ec50-133">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ec50-134">-Ad</span><span class="sxs-lookup"><span data-stu-id="4ec50-134">-Name</span></span>
<span data-ttu-id="4ec50-135">Web uygulamasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4ec50-135">Specifies the name of the Web App.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ec50-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ec50-136">-ResourceGroupName</span></span>
<span data-ttu-id="4ec50-137">Sertifikanın atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4ec50-137">Specifies the name of the resource group that the certificate is assigned to.</span></span>
<span data-ttu-id="4ec50-138">Aynı komutta *Resourcegroupname* parametresini ve *WebApp* parametresini kullanamazsınız.</span><span class="sxs-lookup"><span data-stu-id="4ec50-138">You cannot use the *ResourceGroupName* parameter and the *WebApp* parameter in the same command.</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ec50-139">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="4ec50-139">-Slot</span></span>
<span data-ttu-id="4ec50-140">Web uygulaması dağıtım yuvasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4ec50-140">Specifies the Web App deployment slot.</span></span>
<span data-ttu-id="4ec50-141">Dağıtım yuvası almak için Get-AzureRMWebAppSlot cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="4ec50-141">To get a deployment slot, use the Get-AzureRMWebAppSlot cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ec50-142">-WebApp</span><span class="sxs-lookup"><span data-stu-id="4ec50-142">-WebApp</span></span>
<span data-ttu-id="4ec50-143">Web uygulaması belirtir.</span><span class="sxs-lookup"><span data-stu-id="4ec50-143">Specifies a Web App.</span></span>
<span data-ttu-id="4ec50-144">Web uygulaması edinmek için Get-AzureRmWebApp cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="4ec50-144">To get a Web App, use the Get-AzureRmWebApp cmdlet.</span></span>
<span data-ttu-id="4ec50-145">*WebApp* parametresini, *resourcegroupname* parametresi ve/veya *webappname* ile aynı komutta kullanamazsınız.</span><span class="sxs-lookup"><span data-stu-id="4ec50-145">You cannot use the *WebApp* parameter in the same command as the *ResourceGroupName* parameter and/or the *WebAppName*.</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4ec50-146">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="4ec50-146">-WebAppName</span></span>
<span data-ttu-id="4ec50-147">Web uygulamasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4ec50-147">Specifies the name of the Web App.</span></span>
<span data-ttu-id="4ec50-148">Aynı komutta *Webappname* parametresini ve *WebApp* parametresini kullanamazsınız.</span><span class="sxs-lookup"><span data-stu-id="4ec50-148">You cannot use the *WebAppName* parameter and the *WebApp* parameter in the same command.</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ec50-149">-Onay</span><span class="sxs-lookup"><span data-stu-id="4ec50-149">-Confirm</span></span>
<span data-ttu-id="4ec50-150">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4ec50-150">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ec50-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ec50-151">-WhatIf</span></span>
<span data-ttu-id="4ec50-152">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4ec50-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4ec50-153">Cmdlet çalışmaz. Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4ec50-153">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4ec50-154">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="4ec50-154">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ec50-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ec50-155">CommonParameters</span></span>
<span data-ttu-id="4ec50-156">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4ec50-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ec50-157">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ec50-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ec50-158">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4ec50-158">INPUTS</span></span>

### <span data-ttu-id="4ec50-159">Microsoft. Azure. Management. Web sitesi. modeller. site</span><span class="sxs-lookup"><span data-stu-id="4ec50-159">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="4ec50-160">Parametreler: WebApp (ByValue)</span><span class="sxs-lookup"><span data-stu-id="4ec50-160">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="4ec50-161">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4ec50-161">OUTPUTS</span></span>

### <span data-ttu-id="4ec50-162">System. void</span><span class="sxs-lookup"><span data-stu-id="4ec50-162">System.Void</span></span>

## <span data-ttu-id="4ec50-163">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4ec50-163">NOTES</span></span>

## <span data-ttu-id="4ec50-164">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4ec50-164">RELATED LINKS</span></span>

[<span data-ttu-id="4ec50-165">Get-AzureRmWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="4ec50-165">Get-AzureRmWebAppSSLBinding</span></span>](./Get-AzureRmWebAppSSLBinding.md)

[<span data-ttu-id="4ec50-166">Yeni-AzureRmWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="4ec50-166">New-AzureRmWebAppSSLBinding</span></span>](./New-AzureRmWebAppSSLBinding.md)

[<span data-ttu-id="4ec50-167">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="4ec50-167">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="4ec50-168">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="4ec50-168">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)


