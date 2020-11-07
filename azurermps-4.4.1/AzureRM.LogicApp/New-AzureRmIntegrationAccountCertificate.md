---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: BB1B49CD-B42F-4222-B0BA-0AA4CE3C95E0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/New-AzureRmIntegrationAccountCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/New-AzureRmIntegrationAccountCertificate.md
ms.openlocfilehash: 93136177289d169771dd1ba00ba875f2e7c06c45
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762218"
---
# <span data-ttu-id="c70c0-101">New-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="c70c0-101">New-AzureRmIntegrationAccountCertificate</span></span>

## <span data-ttu-id="c70c0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c70c0-102">SYNOPSIS</span></span>
<span data-ttu-id="c70c0-103">Tümleştirme hesabı sertifikası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c70c0-103">Creates an integration account certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c70c0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c70c0-104">SYNTAX</span></span>

### <span data-ttu-id="c70c0-105">PrivateKey</span><span class="sxs-lookup"><span data-stu-id="c70c0-105">PrivateKey</span></span>
```
New-AzureRmIntegrationAccountCertificate -ResourceGroupName <String> -Name <String> -CertificateName <String>
 -KeyName <String> -KeyVersion <String> -KeyVaultId <String> [-PublicCertificateFilePath <String>]
 [-Metadata <Object>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c70c0-106">PublicKey</span><span class="sxs-lookup"><span data-stu-id="c70c0-106">PublicKey</span></span>
```
New-AzureRmIntegrationAccountCertificate -ResourceGroupName <String> -Name <String> -CertificateName <String>
 [-KeyName <String>] [-KeyVersion <String>] [-KeyVaultId <String>] -PublicCertificateFilePath <String>
 [-Metadata <Object>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c70c0-107">De</span><span class="sxs-lookup"><span data-stu-id="c70c0-107">Both</span></span>
```
New-AzureRmIntegrationAccountCertificate -ResourceGroupName <String> -Name <String> -CertificateName <String>
 -KeyName <String> -KeyVersion <String> -KeyVaultId <String> -PublicCertificateFilePath <String>
 [-Metadata <Object>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c70c0-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="c70c0-108">DESCRIPTION</span></span>
<span data-ttu-id="c70c0-109">**Yeni-AzureRmIntegrationAccountCertificate** cmdlet 'i bir tümleştirme hesabı sertifikası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c70c0-109">The **New-AzureRmIntegrationAccountCertificate** cmdlet creates an integration account certificate.</span></span>
<span data-ttu-id="c70c0-110">Bu cmdlet, tümleştirme hesabı sertifikasını temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="c70c0-110">This cmdlet returns an object that represents the integration account certificate.</span></span>
<span data-ttu-id="c70c0-111">Tümleştirme hesap adını, kaynak grubu adını, sertifika adını, anahtar adını, anahtar sürümü ve Anahtar Kasası KIMLIĞINI belirtin.</span><span class="sxs-lookup"><span data-stu-id="c70c0-111">Specify the integration account name, resource group name, certificate name, key name, key version, and key vault ID.</span></span>
<span data-ttu-id="c70c0-112">Komut satırında belirttiğiniz şablon parametre dosyası değerleri, bir şablon parametre nesnesindeki şablon parametre değerlerinden önceliklidir.</span><span class="sxs-lookup"><span data-stu-id="c70c0-112">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>

<span data-ttu-id="c70c0-113">Bu modül dinamik parametreleri destekler.</span><span class="sxs-lookup"><span data-stu-id="c70c0-113">This module supports dynamic parameters.</span></span>
<span data-ttu-id="c70c0-114">Dinamik parametre kullanmak için, komuta bunu yazın.</span><span class="sxs-lookup"><span data-stu-id="c70c0-114">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="c70c0-115">Dinamik parametrelerin adlarını keşfetmek için, cmdlet adından sonra bir kısa çizgi (-) yazın ve ardından kullanılabilir parametreler arasında geçiş yapmak için SEKME tuşuna art arda basın.</span><span class="sxs-lookup"><span data-stu-id="c70c0-115">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="c70c0-116">Gerekli bir şablon parametresini atlarsanız, cmdlet bu değeri sorar.</span><span class="sxs-lookup"><span data-stu-id="c70c0-116">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="c70c0-117">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c70c0-117">EXAMPLES</span></span>

### <span data-ttu-id="c70c0-118">Örnek 1: Tümleştirme hesabı sertifikası oluşturma</span><span class="sxs-lookup"><span data-stu-id="c70c0-118">Example 1: Create an integration account certificate</span></span>
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

<span data-ttu-id="c70c0-119">Bu komut, belirtilen kaynak grubunda tümleştirme hesabı sertifikasını oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c70c0-119">This command creates the integration account certificate in the specified resource group.</span></span>

## <span data-ttu-id="c70c0-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c70c0-120">PARAMETERS</span></span>

### <span data-ttu-id="c70c0-121">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="c70c0-121">-CertificateName</span></span>
<span data-ttu-id="c70c0-122">Tümleştirme hesabı sertifikası için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="c70c0-122">Specifies a name for the integration account certificate.</span></span>

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

### <span data-ttu-id="c70c0-123">-AnahtarAdı</span><span class="sxs-lookup"><span data-stu-id="c70c0-123">-KeyName</span></span>
<span data-ttu-id="c70c0-124">Anahtar kasasındaki sertifika anahtarının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c70c0-124">Specifies the name of the certificate key in the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: PrivateKey, Both
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: PublicKey
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c70c0-125">-Anahtarlı</span><span class="sxs-lookup"><span data-stu-id="c70c0-125">-KeyVaultId</span></span>
<span data-ttu-id="c70c0-126">Bir anahtar kasa KIMLIĞI belirtir.</span><span class="sxs-lookup"><span data-stu-id="c70c0-126">Specifies a key vault ID.</span></span>

```yaml
Type: System.String
Parameter Sets: PrivateKey, Both
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: PublicKey
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c70c0-127">-KeyVersion</span><span class="sxs-lookup"><span data-stu-id="c70c0-127">-KeyVersion</span></span>
<span data-ttu-id="c70c0-128">Anahtar kasasındaki sertifika anahtarının sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="c70c0-128">Specifies the version of the certificate key in the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: PrivateKey, Both
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: PublicKey
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c70c0-129">-Metadata</span><span class="sxs-lookup"><span data-stu-id="c70c0-129">-Metadata</span></span>
<span data-ttu-id="c70c0-130">Sertifikanın meta veri nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c70c0-130">Specifies a metadata object for the certificate.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c70c0-131">-Ad</span><span class="sxs-lookup"><span data-stu-id="c70c0-131">-Name</span></span>
<span data-ttu-id="c70c0-132">Tümleştirme hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c70c0-132">Specifies the name of an integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c70c0-133">-PublicCertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="c70c0-133">-PublicCertificateFilePath</span></span>
<span data-ttu-id="c70c0-134">Ortak sertifika (. cer) dosyasının yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="c70c0-134">Specifies the path of a public certificate (.cer) file.</span></span>

```yaml
Type: System.String
Parameter Sets: PrivateKey
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: PublicKey, Both
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c70c0-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c70c0-135">-ResourceGroupName</span></span>
<span data-ttu-id="c70c0-136">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c70c0-136">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="c70c0-137">-Onay</span><span class="sxs-lookup"><span data-stu-id="c70c0-137">-Confirm</span></span>
<span data-ttu-id="c70c0-138">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c70c0-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c70c0-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c70c0-139">-WhatIf</span></span>
<span data-ttu-id="c70c0-140">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c70c0-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c70c0-141">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c70c0-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c70c0-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c70c0-142">-DefaultProfile</span></span>
<span data-ttu-id="c70c0-143">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c70c0-143">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c70c0-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c70c0-144">CommonParameters</span></span>
<span data-ttu-id="c70c0-145">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c70c0-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c70c0-146">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c70c0-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c70c0-147">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c70c0-147">INPUTS</span></span>

## <span data-ttu-id="c70c0-148">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c70c0-148">OUTPUTS</span></span>

### <span data-ttu-id="c70c0-149">Microsoft. Azure. Management. Logic. modeller. ıntegrationaccountcertificate</span><span class="sxs-lookup"><span data-stu-id="c70c0-149">Microsoft.Azure.Management.Logic.Models.IntegrationAccountCertificate</span></span>

## <span data-ttu-id="c70c0-150">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c70c0-150">NOTES</span></span>

## <span data-ttu-id="c70c0-151">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c70c0-151">RELATED LINKS</span></span>

[<span data-ttu-id="c70c0-152">Get-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="c70c0-152">Get-AzureRmIntegrationAccountCertificate</span></span>](./Get-AzureRmIntegrationAccountCertificate.md)

[<span data-ttu-id="c70c0-153">Remove-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="c70c0-153">Remove-AzureRmIntegrationAccountCertificate</span></span>](./Remove-AzureRmIntegrationAccountCertificate.md)

[<span data-ttu-id="c70c0-154">Set-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="c70c0-154">Set-AzureRmIntegrationAccountCertificate</span></span>](./Set-AzureRmIntegrationAccountCertificate.md)


