---
title: Azure PowerShell Değişiklik Günlüğü | Microsoft Docs
description: Azure PowerShell'in en son sürümünde yapılan değişikliklerin geçmişi aşağıda verilmiştir.
services: azure
author: sdwheeler
ms.author: sewhee
manager: carmonm
ms.service: azure-powershell
ms.product: azure
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 05/18/2017
ms.openlocfilehash: 143d92384fd270711378f6741ba59e88c12833d1
ms.sourcegitcommit: 37bfbf11fd0967a8e7977c692ab829d286baf88a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/08/2018
---
# <a name="release-notes"></a><span data-ttu-id="52372-103">Sürüm notları</span><span class="sxs-lookup"><span data-stu-id="52372-103">Release notes</span></span>

<span data-ttu-id="52372-104">Azure PowerShell'in bu sürümünde yapılan değişikliklerin listesi aşağıda verilmiştir.</span><span class="sxs-lookup"><span data-stu-id="52372-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

## <a name="version-220"></a><span data-ttu-id="52372-105">Sürüm 2.2.0</span><span class="sxs-lookup"><span data-stu-id="52372-105">Version 2.2.0</span></span>
* <span data-ttu-id="52372-106">İşlem</span><span class="sxs-lookup"><span data-stu-id="52372-106">Compute</span></span>
  - <span data-ttu-id="52372-107">AzureDiskEncryptionForLinux uzantısından sorgu şifreleme durumu için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="52372-107">Add support for querying encryption status from the AzureDiskEncryptionForLinux extension</span></span>
* <span data-ttu-id="52372-108">DataFactory</span><span class="sxs-lookup"><span data-stu-id="52372-108">DataFactory</span></span>
  - <span data-ttu-id="52372-109">Etkinlik pencerelerini listelemek için yeni cmdlet eklendi</span><span class="sxs-lookup"><span data-stu-id="52372-109">Added new cmdlet for listing activity windows</span></span>
    + <span data-ttu-id="52372-110">Get-AzureRmDataFactoryActivityWindow</span><span class="sxs-lookup"><span data-stu-id="52372-110">Get-AzureRmDataFactoryActivityWindow</span></span>
* <span data-ttu-id="52372-111">DataLake</span><span class="sxs-lookup"><span data-stu-id="52372-111">DataLake</span></span>
  - <span data-ttu-id="52372-112">`Host` parametresi `DatabaseHost` olarak değiştirildi ve `Host` parametresine diğer ad eklendi</span><span class="sxs-lookup"><span data-stu-id="52372-112">Changed parameter `Host` to `DatabaseHost` and added alias to `Host`</span></span>
    + <span data-ttu-id="52372-113">New-AzureRmDataLakeAnalyticsCatalogSecret</span><span class="sxs-lookup"><span data-stu-id="52372-113">New-AzureRmDataLakeAnalyticsCatalogSecret</span></span>
    + <span data-ttu-id="52372-114">Set-AzureRmDataLakeAnalyticsCatalogSecret</span><span class="sxs-lookup"><span data-stu-id="52372-114">Set-AzureRmDataLakeAnalyticsCatalogSecret</span></span>
  - <span data-ttu-id="52372-115">ACL ve varsayılan ACL kaldırma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="52372-115">Add support for ACL and Default ACL removal</span></span>
  - <span data-ttu-id="52372-116">Dosya ve klasörler üzerinde adsız izinler alma ve ayarlama desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="52372-116">Add support for getting and setting unnamed permissions on files and folders</span></span>
* <span data-ttu-id="52372-117">KeyVault</span><span class="sxs-lookup"><span data-stu-id="52372-117">KeyVault</span></span>
  - <span data-ttu-id="52372-118">Sertifikalar için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="52372-118">Add support for certificates</span></span>
    + <span data-ttu-id="52372-119">Add-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="52372-119">Add-AzureKeyVaultCertificate</span></span>
    + <span data-ttu-id="52372-120">Add-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="52372-120">Add-AzureKeyVaultCertificateContact</span></span>
    + <span data-ttu-id="52372-121">Get-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="52372-121">Get-AzureKeyVaultCertificate</span></span>
    + <span data-ttu-id="52372-122">Get-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="52372-122">Get-AzureKeyVaultCertificateContact</span></span>
    + <span data-ttu-id="52372-123">Get-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="52372-123">Get-AzureKeyVaultCertificateIssuer</span></span>
    + <span data-ttu-id="52372-124">Get-AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="52372-124">Get-AzureKeyVaultCertificateOperation</span></span>
    + <span data-ttu-id="52372-125">Get-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="52372-125">Get-AzureKeyVaultCertificatePolicy</span></span>
    + <span data-ttu-id="52372-126">Import-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="52372-126">Import-AzureKeyVaultCertificate</span></span>
    + <span data-ttu-id="52372-127">New-AzureKeyVaultCertificateAdministratorDetails</span><span class="sxs-lookup"><span data-stu-id="52372-127">New-AzureKeyVaultCertificateAdministratorDetails</span></span>
    + <span data-ttu-id="52372-128">New-AzureKeyVaultCertificateOrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="52372-128">New-AzureKeyVaultCertificateOrganizationDetails</span></span>
    + <span data-ttu-id="52372-129">New-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="52372-129">New-AzureKeyVaultCertificatePolicy</span></span>
    + <span data-ttu-id="52372-130">Remove-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="52372-130">Remove-AzureKeyVaultCertificate</span></span>
    + <span data-ttu-id="52372-131">Remove-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="52372-131">Remove-AzureKeyVaultCertificateContact</span></span>
    + <span data-ttu-id="52372-132">Remove-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="52372-132">Remove-AzureKeyVaultCertificateIssuer</span></span>
    + <span data-ttu-id="52372-133">Remove-AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="52372-133">Remove-AzureKeyVaultCertificateOperation</span></span>
    + <span data-ttu-id="52372-134">Set-AzureKeyVaultCertificateAttribute</span><span class="sxs-lookup"><span data-stu-id="52372-134">Set-AzureKeyVaultCertificateAttribute</span></span>
    + <span data-ttu-id="52372-135">Set-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="52372-135">Set-AzureKeyVaultCertificateIssuer</span></span>
    + <span data-ttu-id="52372-136">Set-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="52372-136">Set-AzureKeyVaultCertificatePolicy</span></span>
    + <span data-ttu-id="52372-137">Stop-AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="52372-137">Stop-AzureKeyVaultCertificateOperation</span></span>
* <span data-ttu-id="52372-138">Ağ</span><span class="sxs-lookup"><span data-stu-id="52372-138">Network</span></span>

  - <span data-ttu-id="52372-139">+New-AzureRmNetworkInterface -EnableAcceleratedNetworking hızlandırılmış ağ oluşturmayı etkinleştirmek/devre dışı bırakmak üzere ağ arabirimi için yeni anahtar parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="52372-139">New switch parameter added for network interface to enable/disable accelerated networking +New-AzureRmNetworkInterface -EnableAcceleratedNetworking</span></span>
  - <span data-ttu-id="52372-140">Etkin-Etkin ağ geçidi özelliği PowerShell cmdlet’ini etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="52372-140">Enable Active-Active gateway feature PowerShell cmdlets</span></span>
    + <span data-ttu-id="52372-141">Add-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="52372-141">Add-AzureRmVirtualNetworkGatewayIpConfig</span></span>
    + <span data-ttu-id="52372-142">Remove-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="52372-142">Remove-AzureRmVirtualNetworkGatewayIpConfig</span></span>
  - <span data-ttu-id="52372-143">Yeni cmdlet eklendi</span><span class="sxs-lookup"><span data-stu-id="52372-143">Added new cmdlet</span></span>
    + <span data-ttu-id="52372-144">Test-AzureRmPrivateIpAddressAvailability</span><span class="sxs-lookup"><span data-stu-id="52372-144">Test-AzureRmPrivateIpAddressAvailability</span></span>
* <span data-ttu-id="52372-145">Kaynaklar</span><span class="sxs-lookup"><span data-stu-id="52372-145">Resources</span></span>
  - <span data-ttu-id="52372-146">Sağlayıcı ve kaynak cmdlet'lerinde destek bölgeleri</span><span class="sxs-lookup"><span data-stu-id="52372-146">Support zones in provider and resource cmdlets</span></span>
    + <span data-ttu-id="52372-147">Get-AzureRmProvider</span><span class="sxs-lookup"><span data-stu-id="52372-147">Get-AzureRmProvider</span></span>
    + <span data-ttu-id="52372-148">New-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="52372-148">New-AzureRmResource</span></span>
    + <span data-ttu-id="52372-149">Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="52372-149">Set-AzureRmResource</span></span>
* <span data-ttu-id="52372-150">Sql</span><span class="sxs-lookup"><span data-stu-id="52372-150">Sql</span></span>
  - <span data-ttu-id="52372-151">Sunucu düzeyinde Azure SQL tehdit algılama ilkesi yönetimine yönelik yeni cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="52372-151">Added new cmdlets for Azure SQL threat detection policy management at server level</span></span>
    + <span data-ttu-id="52372-152">Get-AzureRmSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="52372-152">Get-AzureRmSqlServerThreatDetectionPolicy</span></span>
    + <span data-ttu-id="52372-153">Remove-AzureRmSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="52372-153">Remove-AzureRmSqlServerThreatDetectionPolicy</span></span>
    + <span data-ttu-id="52372-154">Set-AzureRmSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="52372-154">Set-AzureRmSqlServerThreatDetectionPolicy</span></span>
  - <span data-ttu-id="52372-155">Sql Azure DataWarehouses için GeoBackupPolicy etkinleştirmeyi/devre dışı bırakmayı destekleyen yeni cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="52372-155">Added new cmdlets to support enabling/disabling GeoBackupPolicy for Sql Azure DataWarehouses</span></span>
    + <span data-ttu-id="52372-156">Get-AzureRmSqlDatabaseGeoBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="52372-156">Get-AzureRmSqlDatabaseGeoBackupPolicy</span></span>
    + <span data-ttu-id="52372-157">Set-AzureRmSqlDatabaseGeoBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="52372-157">Set-AzureRmSqlDatabaseGeoBackupPolicy</span></span>
  - <span data-ttu-id="52372-158">Azure Sql Danışmanları ve Önerilen Eylem API’leri için yeni cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="52372-158">Added new cmdlets for Azure Sql Advisors and Recommended Actions APIs</span></span>
    + <span data-ttu-id="52372-159">Get-AzureRmSqlDatabaseAdvisor</span><span class="sxs-lookup"><span data-stu-id="52372-159">Get-AzureRmSqlDatabaseAdvisor</span></span>
    + <span data-ttu-id="52372-160">Get-AzureRmSqlElasticPoolAdvisor</span><span class="sxs-lookup"><span data-stu-id="52372-160">Get-AzureRmSqlElasticPoolAdvisor</span></span>
    + <span data-ttu-id="52372-161">Get-AzureRmSqlServerAdvisor</span><span class="sxs-lookup"><span data-stu-id="52372-161">Get-AzureRmSqlServerAdvisor</span></span>
    + <span data-ttu-id="52372-162">Get-AzureRmSqlDatabaseRecommendedActions</span><span class="sxs-lookup"><span data-stu-id="52372-162">Get-AzureRmSqlDatabaseRecommendedActions</span></span>
    + <span data-ttu-id="52372-163">Get-AzureRmSqlElasticPoolRecommendedActions</span><span class="sxs-lookup"><span data-stu-id="52372-163">Get-AzureRmSqlElasticPoolRecommendedActions</span></span>
    + <span data-ttu-id="52372-164">Get-AzureRmSqlServerRecommendedActions</span><span class="sxs-lookup"><span data-stu-id="52372-164">Get-AzureRmSqlServerRecommendedActions</span></span>
    + <span data-ttu-id="52372-165">Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="52372-165">Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus</span></span>
    + <span data-ttu-id="52372-166">Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="52372-166">Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus</span></span>
    + <span data-ttu-id="52372-167">Set-AzureRmSqlServerAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="52372-167">Set-AzureRmSqlServerAdvisorAutoExecuteStatus</span></span>
    + <span data-ttu-id="52372-168">Set-AzureRmSqlDatabaseRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="52372-168">Set-AzureRmSqlDatabaseRecommendedActionState</span></span>
    + <span data-ttu-id="52372-169">Set-AzureRmSqlElasticPoolRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="52372-169">Set-AzureRmSqlElasticPoolRecommendedActionState</span></span>
    + <span data-ttu-id="52372-170">Set-AzureRmSqlServerRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="52372-170">Set-AzureRmSqlServerRecommendedActionState</span></span>
