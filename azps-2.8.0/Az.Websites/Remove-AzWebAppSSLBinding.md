---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 3AB3D398-E5DB-4214-BA27-6E3B7D225550
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/remove-azwebappsslbinding
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppSSLBinding.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppSSLBinding.md
ms.openlocfilehash: fda088ff8e8b3942ca6dbf94605b3887e3f6884b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93934393"
---
# <span data-ttu-id="e9556-101">Remove-AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="e9556-101">Remove-AzWebAppSSLBinding</span></span>

## <span data-ttu-id="e9556-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e9556-102">SYNOPSIS</span></span>
<span data-ttu-id="e9556-103">Karşıya yüklenen sertifikadan SSL bağlamasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="e9556-103">Removes an SSL binding from an uploaded certificate.</span></span>

## <span data-ttu-id="e9556-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e9556-104">SYNTAX</span></span>

### <span data-ttu-id="e9556-105">S1</span><span class="sxs-lookup"><span data-stu-id="e9556-105">S1</span></span>
```
Remove-AzWebAppSSLBinding [-Name] <String> [[-DeleteCertificate] <Boolean>] [-Force]
 [-ResourceGroupName] <String> [-WebAppName] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e9556-106">S2</span><span class="sxs-lookup"><span data-stu-id="e9556-106">S2</span></span>
```
Remove-AzWebAppSSLBinding [-Name] <String> [[-DeleteCertificate] <Boolean>] [-Force] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e9556-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="e9556-107">DESCRIPTION</span></span>
<span data-ttu-id="e9556-108">**Remove-AzWebAppSSLBinding** cmdlet 'i, bir Azure Web uygulamasından güvenli yuva KATMANı (SSL) bağlamasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="e9556-108">The **Remove-AzWebAppSSLBinding** cmdlet removes a Secure Sockets Layer (SSL) binding from an Azure Web App.</span></span>
<span data-ttu-id="e9556-109">SSL bağlamaları bir Web uygulamasını sertifikayla ilişkilendirmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="e9556-109">SSL bindings are used to associate a Web App with a certificate.</span></span>

## <span data-ttu-id="e9556-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e9556-110">EXAMPLES</span></span>

### <span data-ttu-id="e9556-111">Örnek 1: Web uygulamasının SSL bağlamasını kaldırma</span><span class="sxs-lookup"><span data-stu-id="e9556-111">Example 1: Remove an SSL binding for a web app</span></span>
```
PS C:\>Remove-AzWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp" -Name "www.contoso.com"
```

<span data-ttu-id="e9556-112">Bu komut, Web uygulamasının ContosoWebApp için SSL bağlamasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="e9556-112">This command removes the SSL binding for the web app ContosoWebApp.</span></span>
<span data-ttu-id="e9556-113">*Deletecertificate* parametresi dahil olmadığından, SERTIFIKA artık SSL bağlamaları yoksa silinir.</span><span class="sxs-lookup"><span data-stu-id="e9556-113">Since the *DeleteCertificate* parameter is not included, the certificate will be deleted if it no longer has any SSL bindings.</span></span>

### <span data-ttu-id="e9556-114">Örnek 2: sertifikayı kaldırmadan SSL bağlamasını kaldırma</span><span class="sxs-lookup"><span data-stu-id="e9556-114">Example 2: Remove an SSL binding without removing the certificate</span></span>
```
PS C:\>Remove-AzWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp" -Name "www.contoso.com" -DeleteCertificate $False
```

<span data-ttu-id="e9556-115">Bu komut, örnek 1 ' e benzer şekilde, Web uygulamasının ContosoWebApp için SSL bağlamasını da kaldırır.</span><span class="sxs-lookup"><span data-stu-id="e9556-115">Similar to Example 1, this command also removes the SSL binding for the Web App ContosoWebApp.</span></span>
<span data-ttu-id="e9556-116">Bu örnekte, *Deletecertificate* parametresi eklenir ve parametre değeri $false olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="e9556-116">In this case, however, the *DeleteCertificate* parameter is included, and the parameter value is set to $False.</span></span>
<span data-ttu-id="e9556-117">Bu, herhangi bir SSL bağlaması olup olmamasına bakılmaksızın sertifikanın silinmeyeceği anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="e9556-117">That means that the certificate will not be deleted regardless of whether it has any SSL bindings or not.</span></span>

### <span data-ttu-id="e9556-118">Örnek 3: SSL bağlamasını kaldırmak için nesne başvurusu kullanma</span><span class="sxs-lookup"><span data-stu-id="e9556-118">Example 3: Use an object reference to remove an SSL binding</span></span>
```
PS C:\>$WebApp = Get-AzWebApp -Name "ContosoWebApp"
PS C:\> Remove-AzWebAppSSLBinding -WebApp $WebApp -Name "www.contoso.com"
```

<span data-ttu-id="e9556-119">Bu örnekte, Web uygulamasının SSL bağlamasını kaldırmak için Web App Web sitesinin nesne başvurusu kullanılır.</span><span class="sxs-lookup"><span data-stu-id="e9556-119">This example uses an object reference to the Web App website to remove the SSL binding for a Web App.</span></span>
<span data-ttu-id="e9556-120">İlk komut, Get-AzWebApp cmdlet 'ini kullanarak, ContosoWebApp adlı Web uygulamasına nesne başvurusu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e9556-120">The first command uses the Get-AzWebApp cmdlet to create an object reference to the Web App named ContosoWebApp.</span></span>
<span data-ttu-id="e9556-121">Bu nesne başvurusu $WebApp adlı bir değişkende depolanır.</span><span class="sxs-lookup"><span data-stu-id="e9556-121">That object reference is stored in a variable named $WebApp.</span></span>
<span data-ttu-id="e9556-122">İkinci komut, SSL bağlamasını kaldırmak için nesne başvurusu ve **Remove-AzWebAppSSLBinding** cmdlet 'ini kullanır.</span><span class="sxs-lookup"><span data-stu-id="e9556-122">The second command uses the object reference and the **Remove-AzWebAppSSLBinding** cmdlet to remove the SSL binding.</span></span>

## <span data-ttu-id="e9556-123">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e9556-123">PARAMETERS</span></span>

### <span data-ttu-id="e9556-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9556-124">-DefaultProfile</span></span>
<span data-ttu-id="e9556-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e9556-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e9556-126">-DeleteCertificate</span><span class="sxs-lookup"><span data-stu-id="e9556-126">-DeleteCertificate</span></span>
<span data-ttu-id="e9556-127">Kaldırılan SSL bağlaması sertifika tarafından kullanılan tek bağlamadır, gerçekleşecek eylemi belirtir.</span><span class="sxs-lookup"><span data-stu-id="e9556-127">Specifies the action to take place if the SSL binding being removed is the only binding used by the certificate.</span></span>
<span data-ttu-id="e9556-128">*Deletecertificate* $false olarak ayarlanırsa, bağlama silindiğinde sertifika silinmez.</span><span class="sxs-lookup"><span data-stu-id="e9556-128">If *DeleteCertificate* is set to $False, the certificate will not be deleted when the binding is deleted.</span></span>
<span data-ttu-id="e9556-129">*Deletecertificate* $true olarak ayarlanmışsa veya komuta dahil değilse, sertifika SSL bağlamasıyla birlikte silinir.</span><span class="sxs-lookup"><span data-stu-id="e9556-129">If *DeleteCertificate* is set to $True or is not included in the command, the certificate will be deleted along with the SSL binding.</span></span>
<span data-ttu-id="e9556-130">Sertifika yalnızca kaldırılan SSL bağlaması sertifika tarafından kullanılan tek bağlamadır silinir.</span><span class="sxs-lookup"><span data-stu-id="e9556-130">The certificate will only be deleted if the SSL binding being removed is the only binding used by the certificate.</span></span>
<span data-ttu-id="e9556-131">Sertifikada birden fazla bağlama varsa, sertifika *deletecertificate* parametresinin değerinden bağımsız olarak kaldırılamaz.</span><span class="sxs-lookup"><span data-stu-id="e9556-131">If the certificate has more than one binding, the certificate will not be removed regardless of the value of the *DeleteCertificate* parameter.</span></span>

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

### <span data-ttu-id="e9556-132">-Force</span><span class="sxs-lookup"><span data-stu-id="e9556-132">-Force</span></span>
<span data-ttu-id="e9556-133">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="e9556-133">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e9556-134">-Ad</span><span class="sxs-lookup"><span data-stu-id="e9556-134">-Name</span></span>
<span data-ttu-id="e9556-135">Web uygulamasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e9556-135">Specifies the name of the Web App.</span></span>

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

### <span data-ttu-id="e9556-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e9556-136">-ResourceGroupName</span></span>
<span data-ttu-id="e9556-137">Sertifikanın atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e9556-137">Specifies the name of the resource group that the certificate is assigned to.</span></span>
<span data-ttu-id="e9556-138">Aynı komutta *Resourcegroupname* parametresini ve *WebApp* parametresini kullanamazsınız.</span><span class="sxs-lookup"><span data-stu-id="e9556-138">You cannot use the *ResourceGroupName* parameter and the *WebApp* parameter in the same command.</span></span>

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

### <span data-ttu-id="e9556-139">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="e9556-139">-Slot</span></span>
<span data-ttu-id="e9556-140">Web uygulaması dağıtım yuvasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e9556-140">Specifies the Web App deployment slot.</span></span>
<span data-ttu-id="e9556-141">Dağıtım yuvası almak için Get-AzWebAppSlot cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="e9556-141">To get a deployment slot, use the Get-AzWebAppSlot cmdlet.</span></span>

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

### <span data-ttu-id="e9556-142">-WebApp</span><span class="sxs-lookup"><span data-stu-id="e9556-142">-WebApp</span></span>
<span data-ttu-id="e9556-143">Web uygulaması belirtir.</span><span class="sxs-lookup"><span data-stu-id="e9556-143">Specifies a Web App.</span></span>
<span data-ttu-id="e9556-144">Web uygulaması edinmek için Get-AzWebApp cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="e9556-144">To get a Web App, use the Get-AzWebApp cmdlet.</span></span>
<span data-ttu-id="e9556-145">*WebApp* parametresini, *resourcegroupname* parametresi ve/veya *webappname* ile aynı komutta kullanamazsınız.</span><span class="sxs-lookup"><span data-stu-id="e9556-145">You cannot use the *WebApp* parameter in the same command as the *ResourceGroupName* parameter and/or the *WebAppName*.</span></span>

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

### <span data-ttu-id="e9556-146">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="e9556-146">-WebAppName</span></span>
<span data-ttu-id="e9556-147">Web uygulamasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e9556-147">Specifies the name of the Web App.</span></span>
<span data-ttu-id="e9556-148">Aynı komutta *Webappname* parametresini ve *WebApp* parametresini kullanamazsınız.</span><span class="sxs-lookup"><span data-stu-id="e9556-148">You cannot use the *WebAppName* parameter and the *WebApp* parameter in the same command.</span></span>

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

### <span data-ttu-id="e9556-149">-Onay</span><span class="sxs-lookup"><span data-stu-id="e9556-149">-Confirm</span></span>
<span data-ttu-id="e9556-150">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e9556-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e9556-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e9556-151">-WhatIf</span></span>
<span data-ttu-id="e9556-152">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e9556-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e9556-153">Cmdlet çalışmaz. Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e9556-153">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e9556-154">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e9556-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e9556-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9556-155">CommonParameters</span></span>
<span data-ttu-id="e9556-156">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e9556-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9556-157">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e9556-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9556-158">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e9556-158">INPUTS</span></span>

### <span data-ttu-id="e9556-159">Microsoft. Azure. Commands. WebApps. modeller. PSSite</span><span class="sxs-lookup"><span data-stu-id="e9556-159">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="e9556-160">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e9556-160">OUTPUTS</span></span>

### <span data-ttu-id="e9556-161">System. void</span><span class="sxs-lookup"><span data-stu-id="e9556-161">System.Void</span></span>

## <span data-ttu-id="e9556-162">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e9556-162">NOTES</span></span>

## <span data-ttu-id="e9556-163">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e9556-163">RELATED LINKS</span></span>

[<span data-ttu-id="e9556-164">Get-AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="e9556-164">Get-AzWebAppSSLBinding</span></span>](./Get-AzWebAppSSLBinding.md)

[<span data-ttu-id="e9556-165">Yeni-AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="e9556-165">New-AzWebAppSSLBinding</span></span>](./New-AzWebAppSSLBinding.md)

[<span data-ttu-id="e9556-166">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="e9556-166">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="e9556-167">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="e9556-167">Get-AzWebApp</span></span>](./Get-AzWebApp.md)


