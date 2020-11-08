---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: C0086E73-CCB1-4B75-B367-C79E17738122
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccountcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountCertificate.md
ms.openlocfilehash: 46927e25fb4e32aae9ea1870ef9eeaedd5efe008
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93937724"
---
# <span data-ttu-id="4687c-101">Get-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="4687c-101">Get-AzIntegrationAccountCertificate</span></span>

## <span data-ttu-id="4687c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4687c-102">SYNOPSIS</span></span>
<span data-ttu-id="4687c-103">Kaynak grubundan tümleştirme hesabı sertifikalarını alır.</span><span class="sxs-lookup"><span data-stu-id="4687c-103">Gets integration account certificates from a resource group.</span></span>

## <span data-ttu-id="4687c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4687c-104">SYNTAX</span></span>

```
Get-AzIntegrationAccountCertificate [-ResourceGroupName <String>] [-Name <String>] [-CertificateName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4687c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="4687c-105">DESCRIPTION</span></span>
<span data-ttu-id="4687c-106">**Get-Azıntegrationaccountcertificate** cmdlet 'i bir kaynak grubundan tümleştirme hesabı sertifikalarını alır.</span><span class="sxs-lookup"><span data-stu-id="4687c-106">The **Get-AzIntegrationAccountCertificate** cmdlet gets integration account certificates from a resource group.</span></span>
<span data-ttu-id="4687c-107">Tümleştirme hesap adını, kaynak grubu adını ve sertifika adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="4687c-107">Specify the integration account name, resource group name, and certificate name.</span></span>
<span data-ttu-id="4687c-108">Bu modül dinamik parametreleri destekler.</span><span class="sxs-lookup"><span data-stu-id="4687c-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="4687c-109">Dinamik parametre kullanmak için, komuta bunu yazın.</span><span class="sxs-lookup"><span data-stu-id="4687c-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="4687c-110">Dinamik parametrelerin adlarını keşfetmek için, cmdlet adından sonra bir kısa çizgi (-) yazın ve ardından kullanılabilir parametreler arasında geçiş yapmak için SEKME tuşuna art arda basın.</span><span class="sxs-lookup"><span data-stu-id="4687c-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="4687c-111">Gerekli bir şablon parametresini atlarsanız, cmdlet bu değeri sorar.</span><span class="sxs-lookup"><span data-stu-id="4687c-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="4687c-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4687c-112">EXAMPLES</span></span>

### <span data-ttu-id="4687c-113">Örnek 1: Tümleştirme hesabı sertifikası alma</span><span class="sxs-lookup"><span data-stu-id="4687c-113">Example 1: Get an integration account certificate</span></span>
```
PS C:\>Get-AzIntegrationAccountCertificate -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -CertificateName "IntegrationAccountCertificate01"
Id                : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/certificates/IntegrationAccountCertificate01
Name              : IntegrationAccountCertificate01
Type              : Microsoft.Logic/integrationAccounts/certificates
CreatedTime       : 3/26/2016 6:59:07 PM
ChangedTime       : 3/26/2016 6:59:07 PM
KeyName           : TestKey
KeyVersion        : 1.0
KeyVaultId        : /subscriptions/<SubscriptionId/resourcegroups/ResourceGroup11/providers/microsoft.keyvault/vaults/<name>
KeyVaultName      : testkeyvault
KeyVaultName      : testkeyvault
PublicCertificate : 
MetaData          :
```

<span data-ttu-id="4687c-114">Bu komut, IntegrationAccountCertificate01 adlı tümleştirme hesabı sertifikasını alır.</span><span class="sxs-lookup"><span data-stu-id="4687c-114">This command gets the integration account certificate named IntegrationAccountCertificate01.</span></span>

### <span data-ttu-id="4687c-115">Örnek 2: Tümleştirme hesabı sertifikalarını tümleştirme hesap adıyla alma</span><span class="sxs-lookup"><span data-stu-id="4687c-115">Example 2: Get integration account certificates by integration account name</span></span>
```
PS C:\>Get-AzIntegrationAccountCertificate -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31"
Id                : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/certificates/IntegrationAccountCertificate01
Name              : IntegrationAccountCertificate01
Type              : Microsoft.Logic/integrationAccounts/certificates
CreatedTime       : 3/26/2016 6:59:07 PM
ChangedTime       : 3/26/2016 6:59:07 PM
KeyName           : TestKey
KeyVersion        : 1.0
KeyVaultId        : /subscriptions/<SubscriptionId>/resourcegroups/ResourceGroup11/providers/microsoft.keyvault/vaults/<name>
KeyVaultName      : testkeyvault
KeyVaultName      : testkeyvault
PublicCertificate : 
MetaData          :
```

<span data-ttu-id="4687c-116">Bu komut, IntegrationAccount31 adlı tümleştirme hesabı için tümleştirme hesabı sertifikalarını alır.</span><span class="sxs-lookup"><span data-stu-id="4687c-116">This command gets the integration account certificates for the  integration account named IntegrationAccount31.</span></span>

## <span data-ttu-id="4687c-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4687c-117">PARAMETERS</span></span>

### <span data-ttu-id="4687c-118">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="4687c-118">-CertificateName</span></span>
<span data-ttu-id="4687c-119">Tümleştirme hesabı sertifikasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4687c-119">Specifies the name of an integration account certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4687c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4687c-120">-DefaultProfile</span></span>
<span data-ttu-id="4687c-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="4687c-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4687c-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="4687c-122">-Name</span></span>
<span data-ttu-id="4687c-123">Tümleştirme hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4687c-123">Specifies the name of an integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4687c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4687c-124">-ResourceGroupName</span></span>
<span data-ttu-id="4687c-125">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4687c-125">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4687c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4687c-126">CommonParameters</span></span>
<span data-ttu-id="4687c-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4687c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4687c-128">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4687c-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4687c-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4687c-129">INPUTS</span></span>

### <span data-ttu-id="4687c-130">System. String</span><span class="sxs-lookup"><span data-stu-id="4687c-130">System.String</span></span>

## <span data-ttu-id="4687c-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4687c-131">OUTPUTS</span></span>

### <span data-ttu-id="4687c-132">Microsoft. Azure. Management. Logic. modeller. ıntegrationaccountcertificate</span><span class="sxs-lookup"><span data-stu-id="4687c-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccountCertificate</span></span>

## <span data-ttu-id="4687c-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4687c-133">NOTES</span></span>

## <span data-ttu-id="4687c-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4687c-134">RELATED LINKS</span></span>

[<span data-ttu-id="4687c-135">Yeni-az</span><span class="sxs-lookup"><span data-stu-id="4687c-135">New-AzIntegrationAccountCertificate</span></span>](./New-AzIntegrationAccountCertificate.md)

[<span data-ttu-id="4687c-136">Remove-Azıntegrationaccountcertificate</span><span class="sxs-lookup"><span data-stu-id="4687c-136">Remove-AzIntegrationAccountCertificate</span></span>](./Remove-AzIntegrationAccountCertificate.md)

[<span data-ttu-id="4687c-137">Set-Azıntegrationaccountcertificate</span><span class="sxs-lookup"><span data-stu-id="4687c-137">Set-AzIntegrationAccountCertificate</span></span>](./Set-AzIntegrationAccountCertificate.md)

