---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 2021B6BC-7B59-4A88-B1DF-598203F58901
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5e225702238f9a90891db819753a68f728a482f9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105996"
---
# <span data-ttu-id="57125-101">New-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="57125-101">New-AzureRemoteAppCollection</span></span>

## <span data-ttu-id="57125-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="57125-102">SYNOPSIS</span></span>
<span data-ttu-id="57125-103">Azure RemoteApp koleksiyonu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="57125-103">Creates an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="57125-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="57125-104">SYNTAX</span></span>

### <span data-ttu-id="57125-105">Tümparametersets (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="57125-105">AllParameterSets (Default)</span></span>
```
New-AzureRemoteAppCollection [-CollectionName] <String> [-ImageName] <String> [-Plan] <String>
 [[-Location] <String>] [-Description <String>] [-CustomRdpProperty <String>] [-ResourceType <CollectionMode>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="57125-106">AzureVNet</span><span class="sxs-lookup"><span data-stu-id="57125-106">AzureVNet</span></span>
```
New-AzureRemoteAppCollection [-CollectionName] <String> [-ImageName] <String> [-Plan] <String>
 [[-Location] <String>] [-VNetName] <String> [-SubnetName] <String> [-DnsServers <String>] [[-Domain] <String>]
 [[-Credential] <PSCredential>] [-OrganizationalUnit <String>] [-Description <String>]
 [-CustomRdpProperty <String>] [-ResourceType <CollectionMode>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="57125-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="57125-107">DESCRIPTION</span></span>
<span data-ttu-id="57125-108">**Yeni-AzureRemoteAppCollection** cmdlet 'ı bir Azure RemoteApp koleksiyonu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="57125-108">The **New-AzureRemoteAppCollection** cmdlet creates an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="57125-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="57125-109">EXAMPLES</span></span>

### <span data-ttu-id="57125-110">Örnek 1: koleksiyon oluşturma</span><span class="sxs-lookup"><span data-stu-id="57125-110">Example 1: Create a collection</span></span>
```
PS C:\> New-AzureRemoteAppCollection -CollectionName "Contoso" -ImageName "Windows Server 2012 R2" -Plan Standard -Location "West US" -Description CloudOnly
```

<span data-ttu-id="57125-111">Bu komut, bir Azure RemoteApp koleksiyonu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="57125-111">This command creates an Azure RemoteApp collection.</span></span>

### <span data-ttu-id="57125-112">Örnek 2: kimlik bilgilerini kullanarak koleksiyon oluşturma</span><span class="sxs-lookup"><span data-stu-id="57125-112">Example 2: Create a collection using credentials</span></span>
```
PS C:\> $cred = Get-Credential corp.contoso.com\admin
PS C:\> New-AzureRemoteAppCollection -CollectionName "ContosoHybrid" -ImageName "Windows Server 2012 R2" -Plan Standard -VNetName azureVNet -Domain Contoso.com -Credential $cred -Description Hybrid
```

<span data-ttu-id="57125-113">Bu komut, **Get-Credential** cmdlet 'inin kimlik bilgilerini kullanarak bir Azure RemoteApp koleksiyonu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="57125-113">This command creates an Azure RemoteApp collection using a credential from the **Get-Credential** cmdlet.</span></span>

## <span data-ttu-id="57125-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="57125-114">PARAMETERS</span></span>

### <span data-ttu-id="57125-115">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="57125-115">-CollectionName</span></span>
<span data-ttu-id="57125-116">Azure RemoteApp koleksiyonunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="57125-116">Specifies the name of the Azure RemoteApp collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57125-117">-Credential</span><span class="sxs-lookup"><span data-stu-id="57125-117">-Credential</span></span>
<span data-ttu-id="57125-118">Azure RemoteApp sunucularına etki alanınıza katılma izni olan bir hizmet hesabının kimlik bilgilerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="57125-118">Specifies the credentials of a service account that has permission to join the Azure RemoteApp servers to your domain.</span></span>
<span data-ttu-id="57125-119">**PSCredential** nesnesi almak için **Get-Credential** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="57125-119">To obtain a **PSCredential** object, use the **Get-Credential** cmdlet.</span></span>

```yaml
Type: PSCredential
Parameter Sets: AzureVNet
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57125-120">-Customrdpözelliği</span><span class="sxs-lookup"><span data-stu-id="57125-120">-CustomRdpProperty</span></span>
<span data-ttu-id="57125-121">Sürücü yeniden yönlendirmeyi ve diğer ayarları yapılandırmak için kullanılabilecek özel uzak masaüstü Protocal (RDP) özelliklerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="57125-121">Specifies custom Remote Desktop Protocal (RDP) properties which can be used to configure drive redirection and other settings.</span></span>
<span data-ttu-id="57125-122">Ayrıntılar için [Windows Server 'Daki Uzak Masaüstü Hizmetleri 'Ndeki RDP ayarlarına](https://technet.microsoft.com/library/ff393699(v=ws.10).aspx) bakın `(https://technet.microsoft.com/library/ff393699(v=ws.10).aspx)` .  </span><span class="sxs-lookup"><span data-stu-id="57125-122">See [RDP Settings for Remote Desktop Services in Windows Server](https://technet.microsoft.com/library/ff393699(v=ws.10).aspx)  `(https://technet.microsoft.com/library/ff393699(v=ws.10).aspx)` for details.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57125-123">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="57125-123">-Description</span></span>
<span data-ttu-id="57125-124">Nesne için kısa bir açıklama belirtir.</span><span class="sxs-lookup"><span data-stu-id="57125-124">Specifies a short description for the object.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57125-125">-DnsServers</span><span class="sxs-lookup"><span data-stu-id="57125-125">-DnsServers</span></span>
<span data-ttu-id="57125-126">DNS sunucularının IPv4 adreslerinin virgülle ayrılmış listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="57125-126">Specifies a comma-separated list of IPv4 addresses of the DNS servers.</span></span>

```yaml
Type: String
Parameter Sets: AzureVNet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57125-127">-Etki alanı</span><span class="sxs-lookup"><span data-stu-id="57125-127">-Domain</span></span>
<span data-ttu-id="57125-128">RD Oturumu Ana Bilgisayarı sunucularına katılacak Active Directory etki alanı Hizmetleri etki alanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="57125-128">Specifies the name of the Active Directory Domain Services domain to which to join the RD Session Host servers.</span></span>

```yaml
Type: String
Parameter Sets: AzureVNet
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57125-129">-GörüntüAdı</span><span class="sxs-lookup"><span data-stu-id="57125-129">-ImageName</span></span>
<span data-ttu-id="57125-130">Azure RemoteApp şablonu görüntüsünün adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="57125-130">Specifies the name of the Azure RemoteApp template image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57125-131">-Konum</span><span class="sxs-lookup"><span data-stu-id="57125-131">-Location</span></span>
<span data-ttu-id="57125-132">Koleksiyonun Azure bölgesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="57125-132">Specifies the Azure region of the collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57125-133">-OrganizationalUnit</span><span class="sxs-lookup"><span data-stu-id="57125-133">-OrganizationalUnit</span></span>
<span data-ttu-id="57125-134">RD Oturumu Ana Bilgisayarı sunucularına katılacak kuruluş biriminin (OU) adını belirtir; Örneğin, OU = msiz, DC = etkialanım, DC = ParentDomain, DC = com.</span><span class="sxs-lookup"><span data-stu-id="57125-134">Specifies the name of the organizational unit (OU) to which to join the RD Session Host servers, for example, OU=MyOu,DC=MyDomain,DC=ParentDomain,DC=com.</span></span>
<span data-ttu-id="57125-135">OU ve DC gibi öznitelikler büyük harf olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="57125-135">Attributes such as OU and DC must be in uppercase.</span></span>
<span data-ttu-id="57125-136">Koleksiyon oluşturulduktan sonra OU değiştirilemez.</span><span class="sxs-lookup"><span data-stu-id="57125-136">The OU cannot be changed after the collection has been created.</span></span>

```yaml
Type: String
Parameter Sets: AzureVNet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57125-137">-Plan</span><span class="sxs-lookup"><span data-stu-id="57125-137">-Plan</span></span>
<span data-ttu-id="57125-138">Azure RemoteApp koleksiyonu için kullanım sınırlarını tanımlayabileceğiniz planı belirtir.</span><span class="sxs-lookup"><span data-stu-id="57125-138">Specifies the plan for the Azure RemoteApp collection, which may define the usage limits.</span></span>
<span data-ttu-id="57125-139">Planları görmek için **Get-AzureRemoteAppPlan** 'ı kullanın.</span><span class="sxs-lookup"><span data-stu-id="57125-139">Use **Get-AzureRemoteAppPlan** to see the plans available.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57125-140">-Profil</span><span class="sxs-lookup"><span data-stu-id="57125-140">-Profile</span></span>
<span data-ttu-id="57125-141">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="57125-141">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="57125-142">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="57125-142">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57125-143">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="57125-143">-ResourceType</span></span>
<span data-ttu-id="57125-144">Koleksiyonun kaynak türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="57125-144">Specifies the resource type of the collection.</span></span>
<span data-ttu-id="57125-145">Bu parametre için kabul edilebilir değerler: uygulama veya masaüstü.</span><span class="sxs-lookup"><span data-stu-id="57125-145">The acceptable values for this parameter are: App or Desktop.</span></span>

```yaml
Type: CollectionMode
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57125-146">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="57125-146">-SubnetName</span></span>
<span data-ttu-id="57125-147">Sanal ağda, Azure RemoteApp koleksiyonunu oluşturmak için kullanılacak alt ağın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="57125-147">Specifies the name of the subnet in the virtual network to use to create the Azure RemoteApp collection.</span></span>

```yaml
Type: String
Parameter Sets: AzureVNet
Aliases: 

Required: True
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57125-148">-Vağ adı</span><span class="sxs-lookup"><span data-stu-id="57125-148">-VNetName</span></span>
<span data-ttu-id="57125-149">Azure RemoteApp sanal ağının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="57125-149">Specifies the name of an Azure RemoteApp virtual network.</span></span>

```yaml
Type: String
Parameter Sets: AzureVNet
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57125-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57125-150">CommonParameters</span></span>
<span data-ttu-id="57125-151">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="57125-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57125-152">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57125-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57125-153">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="57125-153">INPUTS</span></span>

## <span data-ttu-id="57125-154">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="57125-154">OUTPUTS</span></span>

## <span data-ttu-id="57125-155">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="57125-155">NOTES</span></span>

## <span data-ttu-id="57125-156">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="57125-156">RELATED LINKS</span></span>

[<span data-ttu-id="57125-157">Get-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="57125-157">Get-AzureRemoteAppCollection</span></span>](./Get-AzureRemoteAppCollection.md)

[<span data-ttu-id="57125-158">Get-AzureRemoteAppPlan</span><span class="sxs-lookup"><span data-stu-id="57125-158">Get-AzureRemoteAppPlan</span></span>](./Get-AzureRemoteAppPlan.md)

[<span data-ttu-id="57125-159">Remove-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="57125-159">Remove-AzureRemoteAppCollection</span></span>](./Remove-AzureRemoteAppCollection.md)

[<span data-ttu-id="57125-160">Set-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="57125-160">Set-AzureRemoteAppCollection</span></span>](./Set-AzureRemoteAppCollection.md)

[<span data-ttu-id="57125-161">Update-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="57125-161">Update-AzureRemoteAppCollection</span></span>](./Update-AzureRemoteAppCollection.md)


