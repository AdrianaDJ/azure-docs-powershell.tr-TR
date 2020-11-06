---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: BB1B49CD-B42F-4222-B0BA-0AA4CE3C95E0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/new-azurermintegrationaccountcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/New-AzureRmIntegrationAccountCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/New-AzureRmIntegrationAccountCertificate.md
ms.openlocfilehash: 555da1343813884a1f773d199cb99a188f7efedc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592115"
---
# <span data-ttu-id="25fa1-101">New-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="25fa1-101">New-AzureRmIntegrationAccountCertificate</span></span>

## <span data-ttu-id="25fa1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="25fa1-102">SYNOPSIS</span></span>
<span data-ttu-id="25fa1-103">Tümleştirme hesabı sertifikası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="25fa1-103">Creates an integration account certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="25fa1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="25fa1-104">SYNTAX</span></span>

### <span data-ttu-id="25fa1-105">PrivateKey</span><span class="sxs-lookup"><span data-stu-id="25fa1-105">PrivateKey</span></span>
```
New-AzureRmIntegrationAccountCertificate -ResourceGroupName <String> -Name <String> -CertificateName <String>
 -KeyName <String> -KeyVersion <String> -KeyVaultId <String> [-PublicCertificateFilePath <String>]
 [-Metadata <Object>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="25fa1-106">PublicKey</span><span class="sxs-lookup"><span data-stu-id="25fa1-106">PublicKey</span></span>
```
New-AzureRmIntegrationAccountCertificate -ResourceGroupName <String> -Name <String> -CertificateName <String>
 [-KeyName <String>] [-KeyVersion <String>] [-KeyVaultId <String>] -PublicCertificateFilePath <String>
 [-Metadata <Object>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="25fa1-107">De</span><span class="sxs-lookup"><span data-stu-id="25fa1-107">Both</span></span>
```
New-AzureRmIntegrationAccountCertificate -ResourceGroupName <String> -Name <String> -CertificateName <String>
 -KeyName <String> -KeyVersion <String> -KeyVaultId <String> -PublicCertificateFilePath <String>
 [-Metadata <Object>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="25fa1-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="25fa1-108">DESCRIPTION</span></span>
<span data-ttu-id="25fa1-109">**Yeni-AzureRmIntegrationAccountCertificate** cmdlet 'i bir tümleştirme hesabı sertifikası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="25fa1-109">The **New-AzureRmIntegrationAccountCertificate** cmdlet creates an integration account certificate.</span></span>
<span data-ttu-id="25fa1-110">Bu cmdlet, tümleştirme hesabı sertifikasını temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="25fa1-110">This cmdlet returns an object that represents the integration account certificate.</span></span>
<span data-ttu-id="25fa1-111">Tümleştirme hesap adını, kaynak grubu adını, sertifika adını, anahtar adını, anahtar sürümü ve Anahtar Kasası KIMLIĞINI belirtin.</span><span class="sxs-lookup"><span data-stu-id="25fa1-111">Specify the integration account name, resource group name, certificate name, key name, key version, and key vault ID.</span></span>
<span data-ttu-id="25fa1-112">Komut satırında belirttiğiniz şablon parametre dosyası değerleri, bir şablon parametre nesnesindeki şablon parametre değerlerinden önceliklidir.</span><span class="sxs-lookup"><span data-stu-id="25fa1-112">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>

<span data-ttu-id="25fa1-113">Bu modül dinamik parametreleri destekler.</span><span class="sxs-lookup"><span data-stu-id="25fa1-113">This module supports dynamic parameters.</span></span>
<span data-ttu-id="25fa1-114">Dinamik parametre kullanmak için, komuta bunu yazın.</span><span class="sxs-lookup"><span data-stu-id="25fa1-114">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="25fa1-115">Dinamik parametrelerin adlarını keşfetmek için, cmdlet adından sonra bir kısa çizgi (-) yazın ve ardından kullanılabilir parametreler arasında geçiş yapmak için SEKME tuşuna art arda basın.</span><span class="sxs-lookup"><span data-stu-id="25fa1-115">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="25fa1-116">Gerekli bir şablon parametresini atlarsanız, cmdlet bu değeri sorar.</span><span class="sxs-lookup"><span data-stu-id="25fa1-116">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="25fa1-117">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="25fa1-117">EXAMPLES</span></span>

### <span data-ttu-id="25fa1-118">Örnek 1: Tümleştirme hesabı sertifikası oluşturma</span><span class="sxs-lookup"><span data-stu-id="25fa1-118">Example 1: Create an integration account certificate</span></span>
```
PS C:\>New-AzureRmIntegrationAccountCertificate -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -CertificateName "IntegrationAccountCertificate01" -KeyName "TestKey" -KeyVersion "1.0" -KeyVaultId "/subscriptions/<subscriptionId>/resourcegroups/ResourceGroup11/providers/microsoft.keyvault/vaults/keyvault" -PublicCertificateFilePath "c:\temp\Certificate.cer"
Id                : /subscriptions/<SusbcriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegartionAccount31/certificates/IntegrationAccountCertificate01
Name              : IntegrationAccountCertificate01
Type              : Microsoft.Logic/integrationAccounts/certificates
CreatedTime       : 3/26/2016 6:59:07 PM
ChangedTime       : 3/26/2016 6:59:07 PM
KeyName           : TestKey
KeyVersion        : 1.0
KeyVaultId        : /subscriptions/<SusbcriptionId>/resourcegroups/ResourceGroup11/providers/microsoft.keyvault/vaults/<name>
KeyVaultName      : testkeyvault
KeyVaultName      : testkeyvault
PublicCertificate : 
MetaData          :
```

<span data-ttu-id="25fa1-119">Bu komut, belirtilen kaynak grubunda tümleştirme hesabı sertifikasını oluşturur.</span><span class="sxs-lookup"><span data-stu-id="25fa1-119">This command creates the integration account certificate in the specified resource group.</span></span>

## <span data-ttu-id="25fa1-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="25fa1-120">PARAMETERS</span></span>

### <span data-ttu-id="25fa1-121">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="25fa1-121">-CertificateName</span></span>
<span data-ttu-id="25fa1-122">Tümleştirme hesabı sertifikası için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="25fa1-122">Specifies a name for the integration account certificate.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25fa1-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25fa1-123">-DefaultProfile</span></span>
<span data-ttu-id="25fa1-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="25fa1-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25fa1-125">-AnahtarAdı</span><span class="sxs-lookup"><span data-stu-id="25fa1-125">-KeyName</span></span>
<span data-ttu-id="25fa1-126">Anahtar kasasındaki sertifika anahtarının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="25fa1-126">Specifies the name of the certificate key in the key vault.</span></span>

```yaml
Type: String
Parameter Sets: PrivateKey, Both
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: PublicKey
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25fa1-127">-Anahtarlı</span><span class="sxs-lookup"><span data-stu-id="25fa1-127">-KeyVaultId</span></span>
<span data-ttu-id="25fa1-128">Bir anahtar kasa KIMLIĞI belirtir.</span><span class="sxs-lookup"><span data-stu-id="25fa1-128">Specifies a key vault ID.</span></span>

```yaml
Type: String
Parameter Sets: PrivateKey, Both
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: PublicKey
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25fa1-129">-KeyVersion</span><span class="sxs-lookup"><span data-stu-id="25fa1-129">-KeyVersion</span></span>
<span data-ttu-id="25fa1-130">Anahtar kasasındaki sertifika anahtarının sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="25fa1-130">Specifies the version of the certificate key in the key vault.</span></span>

```yaml
Type: String
Parameter Sets: PrivateKey, Both
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: PublicKey
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25fa1-131">-Metadata</span><span class="sxs-lookup"><span data-stu-id="25fa1-131">-Metadata</span></span>
<span data-ttu-id="25fa1-132">Sertifikanın meta veri nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="25fa1-132">Specifies a metadata object for the certificate.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25fa1-133">-Ad</span><span class="sxs-lookup"><span data-stu-id="25fa1-133">-Name</span></span>
<span data-ttu-id="25fa1-134">Tümleştirme hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="25fa1-134">Specifies the name of an integration account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25fa1-135">-PublicCertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="25fa1-135">-PublicCertificateFilePath</span></span>
<span data-ttu-id="25fa1-136">Ortak sertifika (. cer) dosyasının yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="25fa1-136">Specifies the path of a public certificate (.cer) file.</span></span>

```yaml
Type: String
Parameter Sets: PrivateKey
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: PublicKey, Both
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25fa1-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25fa1-137">-ResourceGroupName</span></span>
<span data-ttu-id="25fa1-138">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="25fa1-138">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25fa1-139">-Onay</span><span class="sxs-lookup"><span data-stu-id="25fa1-139">-Confirm</span></span>
<span data-ttu-id="25fa1-140">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="25fa1-140">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25fa1-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="25fa1-141">-WhatIf</span></span>
<span data-ttu-id="25fa1-142">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="25fa1-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="25fa1-143">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="25fa1-143">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25fa1-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25fa1-144">CommonParameters</span></span>
<span data-ttu-id="25fa1-145">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="25fa1-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25fa1-146">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25fa1-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25fa1-147">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="25fa1-147">INPUTS</span></span>

### <span data-ttu-id="25fa1-148">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="25fa1-148">None</span></span>
<span data-ttu-id="25fa1-149">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="25fa1-149">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="25fa1-150">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="25fa1-150">OUTPUTS</span></span>

### <span data-ttu-id="25fa1-151">Microsoft. Azure. Management. Logic. modeller. ıntegrationaccountcertificate</span><span class="sxs-lookup"><span data-stu-id="25fa1-151">Microsoft.Azure.Management.Logic.Models.IntegrationAccountCertificate</span></span>

## <span data-ttu-id="25fa1-152">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="25fa1-152">NOTES</span></span>

## <span data-ttu-id="25fa1-153">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="25fa1-153">RELATED LINKS</span></span>

[<span data-ttu-id="25fa1-154">Get-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="25fa1-154">Get-AzureRmIntegrationAccountCertificate</span></span>](./Get-AzureRmIntegrationAccountCertificate.md)

[<span data-ttu-id="25fa1-155">Remove-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="25fa1-155">Remove-AzureRmIntegrationAccountCertificate</span></span>](./Remove-AzureRmIntegrationAccountCertificate.md)

[<span data-ttu-id="25fa1-156">Set-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="25fa1-156">Set-AzureRmIntegrationAccountCertificate</span></span>](./Set-AzureRmIntegrationAccountCertificate.md)


